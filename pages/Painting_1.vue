<template>
  <div class="bg-purple-100 p-4 flex flex-col min-h-screen">
    <CardHolder1 />
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
.paint-icon {
  background: url("/favicon.ico");
}
</style>
