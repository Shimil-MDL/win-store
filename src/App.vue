<template>
  <div>
    <AppStore />
  </div>
</template>

<script>
import AppStore from './components/AppStore.vue'

export default {
  name: "App",
  components: {
    AppStore
    },
}
</script>

<style>
body{

  height: 100vh;
  overflow: hidden;
  background: #030f1f;
	background: radial-gradient(circle,#081832 15%,#030f1f 53%,#04172e 83%);

}
#app {
  font-family: Calibri, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  /* color: #2871b9; */
  margin-top: 60px;

  display: flex;
  justify-content: center;
  align-items: center;
}

</style>
