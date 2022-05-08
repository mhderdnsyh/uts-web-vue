<template>
  <div class="annas">
    <link rel="preconnect" href="https://fonts.googleapis.com" />
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
    <link href="https://fonts.googleapis.com/css2?family=Noto+Naskh+Arabic:wght@600&display=swap" rel="stylesheet" />
    <div class="container my-5">
      <div class="shadow p-3 mb-5 bg-body rounded" style="width: 70rem">
        <h3 class="fw-bold">Surah {{ chapters }}</h3>
        <div class="card-group">
          <div class="container mb-3" style="width: 40rem">
            <p class="btn btn-secondary mt-3" style="width: 100%">Translation {{ chapters }}</p>
            <ul class="text-center" v-for="translate in translate" :key="translate">
              {{
                translate
              }}
            </ul>
          </div>

          <div class="container mb-3" style="width: 18rem">
            <p class="btn btn-secondary mt-3" style="width: 18rem">Reading {{ chapters }}</p>
            <ul class="text-center" v-for="verse in verse" :key="verse">
              {{
                verse
              }}
            </ul>
          </div>
        </div>
      </div>

      <div class="row">
        <div class="container card mb-3" style="width: 22rem">
          <div class="reciter">
            <img src="../assets/img/mishary.jpg" class="card-img-top mt-3" alt="mishary" />
            <div class="card-body">
              <h5 class="card-title">Shaykh Mishary Al-Afasy</h5>
              <p class="card-text"></p>
              <div class="audio">
                <audio controls>
                  <source src="https://download.quranicaudio.com/qdc/mishari_al_afasy/murattal/114.mp3" type="audio/mpeg" />
                  Browsermu tidak mendukung tag audio, upgrade ya!
                </audio>
              </div>
            </div>
            <img src="../assets/img/as-sudais.jpg" class="card-img-top" alt="as-sudais" />
            <div class="card-body">
              <h5 class="card-title">Shaykh Abdurrahman As-Sudais</h5>
              <p class="card-text"></p>
              <div class="audio">
                <audio controls>
                  <source src="https://download.quranicaudio.com/qdc/abdurrahmaan_as_sudais/murattal/114.mp3" type="audio/mpeg" />
                  Browsermu tidak mendukung tag audio, upgrade ya!
                </audio>
              </div>
            </div>
            <img src="../assets/img/hani-ar-rifai.jpeg" class="card-img-top" alt="hani-ar-rifai" />
            <div class="card-body">
              <h5 class="card-title">Shaykh Hani Ar-Rifai</h5>
              <p class="card-text"></p>
              <div class="audio">
                <audio controls>
                  <source src="https://download.quranicaudio.com/qdc/hani_ar_rifai/murattal/114.mp3" type="audio/mpeg" />
                  Browsermu tidak mendukung tag audio, upgrade ya!
                </audio>
              </div>
            </div>
          </div>
        </div>

        <div class="col-lg-8 pt-4 pt-lg-0 content">
          <h3 class="fw-bold">Tafsir Surah {{ chapters }}</h3>
          <p>
            Imam Jalaluddin Al-Mahalli rahimahullah berkata, <br /><br />قُلْ أَعُوذُ بِرَبِّ الناس خالقهم ومالكهم خُصُّو بالذكر تشريفاً لهم ومناسبة للاستفادة من شر الموسوس في صدورهم .<br /><br />
            “Katakanlah: “Aku berlindung kepada Rabb (yang memelihara dan menguasai) manusia”, maksudnya yang mencipta mereka, memiliki mereka. Di sini manusia disebutkan secara khusus sebagai bentuk pemuliaan kepada mereka dan sekaligus
            untuk menyesuaikan dengan pengertian kejahatan waswas setan dalam hati mereka.
          </p>

          <p>
            { مَلِكِ الناس } .<br /><br />
            “Raja manusia.” <br /><br />{ إله الناس } بدلان أو صفتان أو عطفا بيان وأظهر المضاف اليه فيهما زيادة للبيان .<br /><br />
            “Sembahan manusia”, ini sebagai badal atau sifat atau athaf bayan. Tambahan mudhaf ilaih dengan kata manusia sebagai penjelasan. <br /><br />{ مِن شَرِّ الوسواس } أي الشيطان سمي بالحدث لكثرة ملابسته له { الخناس } لأنه يخنس
            ويتأخر عن القلب كلما ذُكِرَ الله . <br /><br />“Dari kejahatan bisikan setan (syarril waswaas)”, disebutkan bisikan setan karena kebanyakan godaan yang dilancarkannya itu melalui bisikan. “Yang bersembunyi (al-khannaas)”,
            maksudnya setan itu bersembunyi dan meninggalkan hati manusia apabila hati manusia ingat kepada Allah.
          </p>
          <p>
            { الَّذِي يُوَسْوِسُ فِي صُدُوِر النَّاسِ } قلوبهم إذا غفلوا عن ذكر الله .<br /><br />

            “Yang membisikkan kejahatan ke dalam dada manusia”, ke dalam kalbu manusia di kala mereka lalai mengingat Allah.<br /><br />

            { مِنَ الجنة والناس } باين للشيطان الموسوس أنه جني أوإنسي ، كقوله تعالى : { شَيَاطِينَ الإِنْسِ وَالجِنِّ } أو من الجنة بيان له ( والناس ) عطف على ( الوسواس ) وعلى كل شمل شر لبيد وبناته المذكورين ، واعترض الأول بأن الناس لا
            يوسوس في صدورهم الناس إنما يوسوس في صدورهم الجن ، وأُجيب بأن الناس يوسوسون أيضاً بمعنى يليق بهم في الظاهر ثم تصل وسوستهم إلى القلب وتثبت فيه بالطريق المؤدي إلى ذلك والله تعالى أعلم .<br /><br />

            “Dari jin dan manusia”, lafaz ayat ini menjelaskan pengertian setan yang menggoda itu, yaitu terdiri dari jenis jin dan manusia, sebagaimana yang dijelaskan dalam ayat lainnya, yaitu melalui firman-Nya,<br /><br />

            شَيَٰطِينَ ٱلْإِنسِ وَٱلْجِنِّ

            <br /><br />“yaitu setan-setan (dari jenis) manusia dan (dan jenis) jin.” (QS. Al-An’am: 112).
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      verse: [],
      chapters: [],
      translate: [],
      audio: [],
    };
  },
  async mounted() {
    const url = await axios.get("https://api.quran.com/api/v4/quran/verses/uthmani?chapter_number=114");
    this.verse = url.data.verses.map(({ text_uthmani }) => text_uthmani);

    const chapters = await axios.get("https://api.quran.com/api/v4/chapters/114?language=id");
    this.chapters = chapters.data.chapter.name_complex;

    const translate = await axios.get("https://api.quran.com/api/v4/quran/translations/134?chapter_number=114");
    this.translate = translate.data.translations.map(({ text }) => text);
    console.log(this.verse);
  },
};
</script>

<style>
.annas {
  color: black;
  text-align: center;
  font-family: "Noto Naskh Arabic", serif;
  font-size: 20px;
}
.judul {
  text-align: center;
}
h3 {
  color: #3b4249;
}
h5 {
  font-weight: bold;
  font-family: "Noto Naskh Arabic";
}
</style>
