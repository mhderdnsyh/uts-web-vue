<template>
  <div class="alikhlas">
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
                  <source src="https://download.quranicaudio.com/qdc/mishari_al_afasy/murattal/112.mp3" type="audio/mpeg" />
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
                  <source src="https://download.quranicaudio.com/qdc/abdurrahmaan_as_sudais/murattal/112.mp3" type="audio/mpeg" />
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
                  <source src="https://download.quranicaudio.com/qdc/hani_ar_rifai/murattal/112.mp3" type="audio/mpeg" />
                  Browsermu tidak mendukung tag audio, upgrade ya!
                </audio>
              </div>
            </div>
          </div>
        </div>

        <div class="col-lg-8 pt-4 pt-lg-0 content">
          <h3 class="fw-bold">Tafsir Surah {{ chapters }}</h3>
          <p>
            Imam Jalaluddin Al-Mahalli rahimahullah berkata,<br /><br />
            سُئِلَ النَّبِيُّ صَلَّى اللهُ عَلَيْهِ وَسَلَّمَ عَنْ رَبِّهِ فَنَزَلَ:<br /><br />
            { قُلْ هُوَ الله أَحَدٌ } فَاللهُ خَبَرُ «هُوَ» وَ «أَحَدٌ» بَدَلٌ مِنْهُ أَوْ خَبَرٌ ثَانٍ . <br /><br />Nabi shallallahu ‘alaihi wa sallam pernah ditanya tentang Rabbnya, lantas turunlah firman Allah: (Katakanlah, “Dialah yang
            Maha Esa”), lafaz jalalah “Allah” adalah khabar dari lafaz “huwa”, sedangkan lafaz “ahadun” adalah badal dari lafaz jalalah “Allah”, atau khabar kedua dari lafaz “huwa”.
          </p>

          <p>
            { اللهُ الصَّمَدُ } مُبْتَدَأٌ وَخَبَرٌ : أَيْ المَقْصُوْدُ فِي الحَوَائِجِ عَلَى الدَّوَامِ .<br /><br />
            (Allah adalah Tuhan yang bergantung kepada-Nya segala sesuatu), lafaz ayat ini terdiri dari mubtada dan khabar (lafaz jalalah “Allah” adalah mubtada dan “Ash-Shamad” adalah khabar). Kalimat tersebut berarti Allah adalah Tuhan
            yang bergantung kepada-Nya segala sesuatu untuk selama-selamanya.
          </p>
          <p>
            { لَمْ يَلِدْ } لاِنْتِفَاءِ مُجَانِسَتِهِ . { وَلَمْ يُولَدْ } لاِنْتِفَاءِ الحُدُوْثِ عَنْهُ . <br /><br />(Dia tiada beranak), karena tiada yang menyamai Allah atau sejenis dengan Allah, (dan tidak pula diperanakkan) karena
            mustahil hal ini terjadi bagi-Nya.
          </p>
          <p>
            { وَلَمْ يَكُنْ لَّهُ كُفُواً أَحَدٌ } أَيْ مُكَافِئاً ومُمَاثِلاً وَ «لَهُ» مُتَعَلِّقٌ بِ «كُفَواً» وَقُدِّم عَلَيْهِ لِأَنَّهُ مَحَطُّ القَصْدِ بِالنَّفْيِ ، وَأُخِّرَ «أَحَدٌ» وَهُوَ اِسْمُ «يَكُنْ» عَنْ خَبَرِهَا رِعَايَةً
            لِلفَاصِلَةِ .<br /><br />

            (Dan tidak ada seorang pun yang setara dengan Allah), atau yang semisal dengan-Nya. Lafaz “lahu” berkaitan (muta’alliq) kepada lafaz “kufuwan”. Lafaz “lahu” ini didahulukan karena dialah yang menjadi subjek penafian. Kemudian
            lafaz “ahadun” diakhirkan letaknya padahal ia sebagai isim dari lafaz “yakun”, sedangkan khabar yang seharusnya berada di akhir mendahuluinya. Demikian itu karena menjaga fasilah atau kesamaan bunyi pada akhir ayat.
          </p>
          <p>
            Sebab turun surat al-Ikhlâs ini adalah pertanyaan orang-orang kafir tentang Allâh Azza wa Jalla , sebagaimana disebutkan di dalam hadits :<br /><br />
            عَنْ أُبَيِّ بْنِ كَعْبٍ أَنَّ الْمُشْرِكِينَ قَالُوا لِرَسُولِ اللَّهِ صَلَّى اللَّهُ عَلَيْهِ وَسَلَّمَ انْسُبْ لَنَا رَبَّكَ فَأَنْزَلَ اللَّهُ قُلْ هُوَ اللَّهُ أَحَدٌ اللَّهُ الصَّمَدُ <br /><br />Dari Ubayy bin Ka’ab
            Radhiyallahu anhu bahwa orang-orang musyrik berkata kepada Rasûlullâh Shallallahu ‘alaihi wa sallam , “Sebutkan nasab Rabbmu kepada kami!”, maka Allâh menurunkan: (Katakanlah: “Dia-lah Allâh, yang Maha Esa). [HR. Tirmidzi, no:
            3364; Ahmad, no: 20714; Ibnu Abi ‘Ashim di dalam as-Sunnah 1/297. Dihasankan oleh Syaikh al-Albani] Hadits ini menunjukkan bahwa surat al-Ikhlâs termasuk surat Makiyyah, dan nampaknya termasuk surat yang awal turun di kota
            Makkah.
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
    const url = await axios.get("https://api.quran.com/api/v4/quran/verses/uthmani?chapter_number=112");
    this.verse = url.data.verses.map(({ text_uthmani }) => text_uthmani);

    const chapters = await axios.get("https://api.quran.com/api/v4/chapters/112?language=id");
    this.chapters = chapters.data.chapter.name_complex;

    const translate = await axios.get("https://api.quran.com/api/v4/quran/translations/134?chapter_number=112");
    this.translate = translate.data.translations.map(({ text }) => text);
    console.log(this.verse);
  },
};
</script>

<style>
.alikhlas {
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
