<template>
  <div class="feedback my-3">
    <h5>Give Feedback</h5>
    <div class="btn-toolbar text-center well mt-3">
      <button type="button" class="btn btn-light btn-color btn-bg-color col-xs-3"><span class="glyphicon glyphicon-plus" aria-hidden="true"></span> Feature Request<span class="badge bg-secondary">138</span></button>
      <button type="button" class="btn btn-light btn-color btn-bg-color col-xs-3 mt-2"><span class="glyphicon glyphicon-time" aria-hidden="true"></span> Tafsir Request<span class="badge bg-secondary">17</span></button>
      <button type="button" class="btn btn-light btn-color btn-bg-color col-xs-3 mt-2"><span class="glyphicon glyphicon-edit" aria-hidden="true"></span> Bugs<span class="badge bg-secondary">65</span></button>
    </div>
    <div class="btn-toolbar text-center well mt-3">
      <button type="button" class="btn btn-light btn-color btn-bg-color col-xs-3 mt-1"><span class="glyphicon glyphicon-plus" aria-hidden="true"></span> Translations and Reciters<span class="badge bg-secondary">30</span></button>
      <button type="button" class="btn btn-light btn-color btn-bg-color col-xs-3 mt-2"><span class="glyphicon glyphicon-edit" aria-hidden="true"></span> Translations and Tafsir errors<span class="badge bg-secondary">15</span></button>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.feedback {
  margin-left: 5rem;
}
h5 {
  color: rgb(71, 70, 70);
}
.btn-toolbar .btn {
  margin-right: 5rem;
  text-align: left;
}

span {
  margin-left: 15px;
}
</style>
