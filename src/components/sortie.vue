<template>
<div id="sortie">

  <h2>{{affiche.show_title}}</h2>
  <div class="container">
    <div class="row mt-5 mb-5">
      <div class="col-6">
        <img :src="affiche.poster" alt="" class="col-12">
      </div>
      <div class="col-6">
        <p class="p1 col-10">{{affiche.summary}}</p>
      </div>
    </div>
  </div>
</div>
</template>

<script>
export default {
  name: 'sortie',
  props: ['affiche']
}
</script>

<style>
h2 {
  color: white;
  font-size: 60px;
}

.p1 {
  color: white;
  font-size: 21px;
  margin-top: 50px;
  margin-bottom: 20px;
  width: 80%;
  margin-left: 20px;
}
</style>
