<template lang="">
  <div class="logo">
    <img class="img" :src="image" :alt="image">
  </div>
</template>


<script>

export default{
  name: 'Main',


  data() {
    return {
      image: "/Icons/logo.jpg"
    }
  },
}

</script>


<style scoped>

.img{
  width: 100%;
  height: 28vw;
  margin: 50px 0;
}

.logo{
  width: 100%;
  text-align: center;
}

</style>