<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Qur'an</a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarSupportedContent">
          <ul class="navbar-nav me-auto mb-2 mb-lg-0">
            <li class="nav-link">
              <router-link to="/">Home</router-link>
            </li>
            <li class="nav-link">
              <router-link to="/daftarsurah">Surah 3 Qul</router-link>
            </li>
            <li class="nav-item dropdown">
              <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-bs-toggle="dropdown" aria-expanded="false"> Daftar Surah </a>
              <ul class="dropdown-menu" aria-labelledby="navbarDropdown">
                <li></li>
                <li class="dropdown-item">
                  <router-link to="/annas">An-Nas</router-link>
                </li>
                <li><hr class="dropdown-divider" /></li>
                <li class="dropdown-item">
                  <router-link to="/disable">Al-Ikhlas</router-link>
                </li>
                <li><hr class="dropdown-divider" /></li>
                <li class="dropdown-item">
                  <router-link to="/allsurah">All Surah</router-link>
                </li>
              </ul>
            </li>
            <li class="nav-link">
              <router-link to="/pengaturan">Pengaturan</router-link>
            </li>
            <li class="nav-link">
              <router-link to="/feedback">Feedback</router-link>
            </li>
          </ul>

          <div class="d-flex">
            <button type="button" class="btn btn-light shadow-sm position-relative">
              Patch v5.0
              <span class="position-absolute top-0 start-60 translate-middle badge rounded-pill bg-danger">
                10+
                <span class="visually-hidden">unread messages</span>
              </span>
            </button>
          </div>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>

<style>
@import url("https://fonts.googleapis.com/css?family=Quicksand:400,700&display=swap");

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* text-align: center; */
  color: white;
  /* margin-top: 60px; */
  padding: 0;
  margin: 0;
}

nav {
  font-family: "Trebuchet MS";
}

nav a:hover {
  border-bottom: 2px solid #000000;
  color: #4d5c77;
}

nav a.router-link-exact-active {
  color: rgb(10, 3, 3);
}
</style>
