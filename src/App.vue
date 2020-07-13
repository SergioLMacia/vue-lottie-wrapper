<template>
  <div id="app">
    <HelloWorld msg="Hello Lottie in Vue!"/>
    <h2>Lottie estático</h2>
    <Lottie
      src="https://assets10.lottiefiles.com/private_files/lf30_pKg5bm.json"
      id="staticLottie"
      :autoplay="true"
      :loop="true"
    ></Lottie>
    <h2>Lottie con scroll</h2>
      <Lottie
        id="scrollingLottie"
        src="https://assets9.lottiefiles.com/packages/lf20_Fh701N.json"
        :expandedOptions="{
          mode: 'scroll',
          controls:true,
          actions: [
            {
              visibility: [0, 1],
              type: 'seek',
              frames: [0, 38]
            }
          ],
        }"
      ></Lottie>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Lottie from "./components/Lottie";

export default {
  name: "App",
  components: {
    HelloWorld,
    Lottie
  }
};
</script>

<style>
body {
  background-color: #021f36;
}

#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #fff;
  margin-top: 60px;
}
</style>
