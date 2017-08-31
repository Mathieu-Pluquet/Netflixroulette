<template>
  <div id="entre">
      <img class="img1"src="http://www.journaldugeek.com/wp-content/blogs.dir/1/files/2016/01/netflix-logo1.png" alt="">
  <form v-on:submit="formsub">
    <input class="form1 lol"type="text" placeholder="Search for Movies, TV Shows, Actor and Directors ..." name="" value="" v-model="titre">
    <!-- <input type="submit" name="" value=""> -->
    <button type="submit" name="button">
      <img class="img2" src="http://www.numerama.com/content/uploads/2016/01/13502130_10153696123838870_522765110773053650_n-796x796-2.png" alt="">
    </button>
  </form>
  </div>
</template>

<script>

export default {
  name: 'entre',
  data(){
    return{
      titre:''
    }
  },
  methods:{
    formsub(e){
    this.$emit('formsub',this.titre);
    e.preventDefault()
    $(".lol").val("")
  }
  }
}
</script>

<style media="screen">
.img1 {
  width: 25%;
  height: 20%;
}

.form1 {
  height: 100px;
  width: 80%;
  font-size: 45px;
}

.img2 {
height: 100px;
width: 100px;
}

button {
  background-color: black;
}

form {
  display: flex;
  justify-content: center;
  margin-top: 50px;
}
</style>
