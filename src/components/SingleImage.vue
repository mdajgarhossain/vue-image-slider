<template>
  <div
    :style="{ backgroundImage: 'url(\'' + currentImage.imageUrl + '\')' }"
    class="imageContainer"
  >
    <h1 class="title">{{ currentImage.title }}</h1>
    <p v-if="currentImage.text" class="subtitle">{{ currentImage.text }}</p>
    <button v-if="currentImage.button" class="btn">
      {{ currentImage.button }}
    </button>
  </div>
</template>

<script>
export default {
  name: "SingleImage",
  props: { currentImage: Object },
};
</script>

<style>
.imageContainer {
  height: 600px;
  width: 100%;
  background-repeat: no-repeat;
  background-size: cover;
}
.title {
  font-size: 3em;
  color: #203d2d;
  margin-top: 0%;
  padding-top: 8%;
}
.subtitle {
  font-size: 1.5em;
}
.btn {
  background: #3498db;
  background-image: -webkit-linear-gradient(top, #3498db, #2980b9);
  background-image: -moz-linear-gradient(top, #3498db, #2980b9);
  background-image: -ms-linear-gradient(top, #3498db, #2980b9);
  background-image: -o-linear-gradient(top, #3498db, #2980b9);
  background-image: linear-gradient(to bottom, #3498db, #2980b9);
  -webkit-border-radius: 0;
  -moz-border-radius: 0;
  border-radius: 0px;
  font-family: Arial;
  color: #e9e9e9;
  font-size: 20px;
  padding: 8px 18px 8px 18px;
  text-decoration: none;
}

.btn:hover {
  background: #3cb0fd;
  background-image: -webkit-linear-gradient(top, #3cb0fd, #3498db);
  background-image: -moz-linear-gradient(top, #3cb0fd, #3498db);
  background-image: -ms-linear-gradient(top, #3cb0fd, #3498db);
  background-image: -o-linear-gradient(top, #3cb0fd, #3498db);
  background-image: linear-gradient(to bottom, #3cb0fd, #3498db);
  text-decoration: none;
  cursor: pointer;
}
</style>
