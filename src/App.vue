<template>
  <div id="app">
    <Slider :images="images" />
  </div>
</template>

<script>
import Slider from "./components/Slider.vue";

export default {
  name: "App",
  components: {
    Slider,
  },
  data() {
    return {
      images: [
        "https://cdn.pixabay.com/photo/2021/03/12/12/28/beach-6089501_960_720.jpg",
        "https://cdn.pixabay.com/photo/2021/04/11/12/11/plum-blossom-6169571_960_720.jpg",
        "https://cdn.pixabay.com/photo/2021/01/11/08/53/sky-5907605_960_720.jpg",
        "https://cdn.pixabay.com/photo/2020/08/10/11/22/mountains-5477557_960_720.jpg",
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

body {
  margin: 0px;
}
</style>
