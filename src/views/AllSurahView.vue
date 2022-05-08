<template>
  <div class="allsurah ms-3">
    <link href="https://fonts.googleapis.com/css2?family=Noto+Naskh+Arabic:wght@600&display=swap" rel="stylesheet" />
    <!-- awal button search -->
    <div class="search my-3 d-flex justify-content-center">
      <input type="number" v-model="inputnomor" class="input" placeholder="Cari Surah" />
      <button @click="lihat" class="btn btn-outline-dark btn ms-2">Search</button>
    </div>
    <!-- tutup button search -->

    <div class="row ms-5">
      <h5 class="title text-dark mb-3">Recently Read</h5>
      <div class="col-sm-2">
        <div class="card bg-light mb-3" style="max-width: 18rem">
          <div class="card-header text-secondary fw-bold">Mankind <span class="badge bg-light shadow-sm badge-light text-dark ms-3">114</span></div>
          <div class="card-body">
            <h5 class="card-title text-dark fw-bold">Surah An-Nas</h5>
            <img class="card-img-top" src="../assets/img/an-nas.jpg" alt="Card image cap" />
          </div>
        </div>
      </div>
      <div class="col-sm-2">
        <div class="card bg-light mb-3" style="max-width: 18rem">
          <div class="card-header text-secondary fw-bold">The Sincerity <span class="badge bg-light shadow-sm badge-light text-dark ms-3">112</span></div>
          <div class="card-body">
            <h5 class="card-title text-dark fw-bold">Surah Al-Ikhlas</h5>
            <img class="card-img-top" src="../assets/img/al-ikhlas.jpg" alt="Card image cap" />
          </div>
        </div>
      </div>
    </div>

    <!-- awal chapter -->
    <div class="chapter mt-4">
      <div class="name-surah d-flex justify-content-center">
        <h3 v-if="chapters" class="chapters fw-bold">Surah {{ chapters.name_simple }}</h3>
      </div>
    </div>
    <!-- tutup chapter -->
    <!-- awal verse -->
    <div class="verse mt-3">
      <div class="verses">
        <ul class="container shadow-sm-3 md-5 w-auto">
          <li class="list-group-item verse shadow-sm d-flex justify-content-end mt-3" v-for="verse in verse" :key="verse.id">{{ verse.text_uthmani }} {{ verse.text }}</li>
        </ul>
      </div>
    </div>
    <!-- tutup verse -->
    <!-- awal reciter -->
    <div class="reciter d-flex justify-content-center">
      <p v-if="audio">
        <audio controls class="reciters">
          <source :src="audio.audio_url" type="audio/mpeg" />
          Browsermu tidak mendukung tag audio, upgrade ya!
        </audio>
      </p>
    </div>
    <!-- tutup reciter -->
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      verse: [],
      audio: null,
      chapters: null,
      inputnomor: "",
    };
  },

  methods: {
    async lihat() {
      let nomor = this.inputnomor;
      let verse = `https://api.quran.com/api/v4/quran/verses/uthmani?chapter_number=${nomor}`;
      let translate = "https://api.quran.com/api/v4/quran/translations/134?chapter_number=" + nomor;

      let chapters = "https://api.quran.com/api/v4/chapters?language=en";
      let reciter = "https://api.quran.com/api/v4/chapter_recitations/3?language=en";

      if (nomor <= 0 || nomor > 114) {
        alert("0 search results");
      } else {
        const callVerse = axios.get(verse);
        const callTranslate = axios.get(translate);
        const callChapters = axios.get(chapters);
        const callReciter = axios.get(reciter);

        axios.all([callVerse, callTranslate, callChapters, callReciter]).then(
          axios.spread((...response) => {
            const respVerse = response[0];
            const respTranslate = response[1];
            const respChapters = response[2];
            const respReciter = response[3];

            const x = respVerse.data.verses;
            const y = respTranslate.data.translations;

            const merge = (x, y) => {
              const res = [];

              for (let i = 0; i < x.length + y.length; i++) {
                if (i % 2 === 0) {
                  res.push(x[i / 2]);
                } else {
                  res.push(y[(i - 1) / 2]);
                }
              }
              return res;
            };

            this.verse = merge(x, y);
            this.audio = respReciter.data.audio_files[nomor - 1];
            this.chapters = respChapters.data.chapters[nomor - 1];
          })
        );
      }
    },
  },
};
</script>

<style>
.search {
  font-family: "Trebuchet MS";
}
.h3 {
  text-align: center;
}
.chapters {
  color: #3b4249;
  text-align: justify;
  font-family: "Noto Naskh Arabic";
}
.verses {
  font-family: "Noto Naskh Arabic", serif;
  font-size: 20px;
  text-align: justify;
}
</style>
