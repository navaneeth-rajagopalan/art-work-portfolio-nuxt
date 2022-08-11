<!-- Please remove this file from your project -->
<template>
  <div class="container mx-auto">
    <div class="grid-cols-4 p-0 lg:space-y-0 lg:grid lg:gap-3">
      <div class="w-full col-span-1 my-2 row-span-3 rounded">
        <UserThumbnail></UserThumbnail>
      </div>
      <div class="w-full rounded col-span-3 my-2 p-2 row-span-3">
        <transition-group tag="div" class="img-slider" name="slide">
          <div v-for="number in [currentImg]" v-bind:key="number">
            <img :src="imgList[Math.abs(currentImg) % imgList.length]" />
          </div>
        </transition-group>
      </div>
    </div>
  </div>
</template>

<script>
import UserThumbnail from './UserThumbnail.vue';

export default {
  name: "CardHolder1",
  components: { UserThumbnail },
  data() {
    return {
      message: 'Click for slide',
      show: true,
      imgList: [
        "/img/Painting_2.jpeg",
        "/img/Painting_1/Painting_1_5.jpg",
        "/img/Painting_1/Painting_1_4.jpg",
        "/img/Painting_1/Painting_1_3.jpg",
        "/img/Painting_1/Painting_1_2.jpg",
        "/img/Painting_1/Painting_1_1.jpeg",
        "/img/Painting_2.jpeg",
      ],
      currentImg: 0
    }
  },
  mounted() {
    setInterval(() => {
      this.currentImg = this.currentImg + 1;
    }, 3000);
  }
}
</script>


<style scoped>
#demo {
  overflow: hidden;
}

.slide-leave-active,
.slide-enter-active {
  transition: 1s;
}

.slide-enter {
  transform: translate(100%, 0);
}

.slide-leave-to {
  transform: translate(-100%, 0);
}

.img-slider {
  overflow: hidden;
  position: relative;
  height: calc(100vh - 2rem);
  width: 100%;
}

.img-slider img {
  position: absolute;
  width: 100%;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  object-fit: scale-down;
}
</style>
