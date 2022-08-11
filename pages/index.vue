<template>
  <div class="bg-purple-100 p-4 flex flex-col min-h-screen">
    <UserThumbnail />
    <div class="font-sans w-full px-4 py-5 sm:p-6 text-center text-2xl">
      When beauty creates beauty
    </div>
    <CardHolder />
  </div>
</template>

<script lang="ts">
import Vue from 'vue';
export default {
  name: "IndexPage",
  head() {
    return {
      title: "Pradisa's Art Portfolio",
      meta: [
        {
          hid: "",
          name: "",
          content: "",
        },
      ],
    };
  },
  setup() {
    return {  };
  },
}
</script>

<style scoped>
.backdrop {
  background: url("/img/Canvas_Image.jpg");
}
</style>
