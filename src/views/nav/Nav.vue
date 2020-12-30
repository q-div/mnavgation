<template>
    
</template>

<script>
export default {
    name: "Nav",
    methods: {
      btnShow() {

      }
    }
}
</script>

<style scoped>
   .nav {
      position: absolute;
      right: 0;
      top:50%;
      transform: translateY(-50%);
      width: 25px;
      height: 25px;
      background-color: deeppink;
      border:1px solid pink
  }
  
  .nav-son {
      position: absolute;
      top: 0;
      right: -271px;
      width: 256px;
      height: 568px;
      background-color: blue;
      transition: all 0.5s;

  }
</style>