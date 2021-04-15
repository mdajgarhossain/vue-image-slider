<template>
  <div>
    <transition-group tag="div">
      <div v-for="i in [currentIndex]" :key="i">
        <img :src="currentImage" />
      </div>
    </transition-group>
  </div>
</template>

<script>
export default {
  name: 'Slider',
  data() {
    return {
      images: [
        'https://cdn.pixabay.com/photo/2021/03/12/12/28/beach-6089501_960_720.jpg',
        'https://cdn.pixabay.com/photo/2021/04/11/12/11/plum-blossom-6169571_960_720.jpg',
        'https://cdn.pixabay.com/photo/2021/01/11/08/53/sky-5907605_960_720.jpg'
      ],
      currentIndex: 0,
    }
  },
   computed: {
     currentImage() {
       return this.images && this.images.length && this.images[Math.abs(this.currentIndex) % this.images.length];
     }
   }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
