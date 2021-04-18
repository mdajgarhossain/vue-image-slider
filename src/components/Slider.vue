<template>
  <div>
    <transition-group tag="div" name="fade">
      <div v-for="i in [currentIndex]" :key="i">
        <img :src="currentImage" />
      </div>
    </transition-group>
    <a class="previous" @click="showPreviousSlide" href="#">&#10094;</a>
    <a class="next" @click="showNextSlide" href="#">&#10095;</a>
  </div>
</template>

<script>
export default {
  name: "Slider",
  props: { images: Array },
  data() {
    return {
      currentIndex: 0,
      timer: null,
    };
  },

  computed: {
    currentImage() {
      return (
        this.images &&
        this.images.length &&
        this.images[Math.abs(this.currentIndex) % this.images.length]
      );
    },
  },

  mounted() {
    this.startSlide();
  },

  methods: {
    startSlide() {
      this.timer = setInterval(this.showNextSlide, 5000);
    },

    showNextSlide() {
      this.currentIndex += 1;
    },
    showPreviousSlide() {
      this.currentIndex -= 1;
    },
  },
};
</script>

<style>
.previous,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}
.next {
  right: 0;
}
.previous {
  left: 0;
}
.previous:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.9);
}

img {
  height: 600px;
  width: 100%;
  object-fit: cover;
}
.fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width: 100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width: 100%;
  opacity: 0;
}
</style>
