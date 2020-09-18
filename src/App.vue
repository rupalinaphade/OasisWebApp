<template>
  <div id="app">
    <div id="img">
    <img alt="Oasis" src="./assets/OasisLogo.jpg">
    </div>
    <div id="bodyContent">
    <Home></Home>
      </div>
  
     <footer>
       <div>
      <p>Oasis Engineering - {{new Date().getFullYear()}}</p>
       </div>
    </footer>
  </div>
</template>

<script>
import Home from './components/Home.vue'

export default {
  name: 'App',
  components: {
    Home
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
  margin-top: 60px;
  padding-left: 60px;
  padding-right: 60px;


}
#img{
  position: relative;
  height: 10px;
  width: 100%;

}
#bodyContent{
  position: relative;
  margin-top: 10%;
}
</style>
