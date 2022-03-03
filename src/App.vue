<template>
  <img alt="" src="./assets/pcso.png"> 
  <HelloWorld msg=""/>
</template>

<script>
import HelloWorld from './components/lotto-generator.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 150px;
  margin-left:50px;
}

img{
  height: 50px;
  width:50px;
   margin-bottom: 150px;
  margin-right:400px
}

</style>
