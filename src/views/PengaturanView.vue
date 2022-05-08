<template>
  <div class="pengaturan my-3">
    <div class="theme">
      <h5>Theme</h5>
      <div class="btn-group">
        <a href="#" class="btn btn-secondary active" aria-current="page">Auto</a>
        <a href="#" class="btn btn-light">Light Mode</a>
        <a href="#" class="btn btn-dark">Dark Mode</a>
      </div>
    </div>
    <div class="font mt-3">
      <h5>Qur'an Font</h5>
      <div class="btn-group">
        <a href="#" class="btn btn-secondary active" aria-current="page">Uthmani</a>
        <a href="#" class="btn btn-secondary">IndoPak</a>
        <a href="#" class="btn btn-secondary">Imlaei </a>
      </div>
    </div>
    <div class="audio mt-3">
      <h5>Audio</h5>
      <div class="btn-group" role="group" aria-label="Button group with nested dropdown">
        <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">Repeat Settings</button>
        <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
          <li><a class="dropdown-item" href="#">On</a></li>
          <li><a class="dropdown-item" href="#">Off</a></li>
        </ul>

        <div class="btn-group" role="group">
          <button id="btnGroupDrop1" type="button" class="btn btn-light dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">Selected Reciter</button>
          <ul class="dropdown-menu" aria-labelledby="btnGroupDrop1">
            <li><a class="dropdown-item" href="#">Shaykh Mishary Al-Afasy</a></li>
            <li><a class="dropdown-item" href="#">Shaykh Abdurrahman As-Sudais</a></li>
            <li><a class="dropdown-item" href="#">Shaykh Hani Ar-Rifai</a></li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.pengaturan {
  margin-left: 5rem;
}
h5 {
  color: rgb(71, 70, 70);
}
</style>
