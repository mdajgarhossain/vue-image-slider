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
        {
          title: "Welcome to california",
          imageUrl:
            "https://cdn.pixabay.com/photo/2021/03/12/12/28/beach-6089501_960_720.jpg",
          text: "California, a western U.S. state",
          button: "Get Started",
        },
        {
          title: "Hello there! This is the tech world",
          text:
            "Technology is the sum of techniques, skills, methods, and processes",
          imageUrl:
            "https://cdn.pixabay.com/photo/2018/02/23/04/38/laptop-3174729_960_720.jpg",
        },
        {
          imageUrl:
            "https://cdn.pixabay.com/photo/2019/07/14/16/29/pen-4337524_960_720.jpg",
        },
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
