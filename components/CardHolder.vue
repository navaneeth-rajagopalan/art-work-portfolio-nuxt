<!-- Please remove this file from your project -->
<template>
  <div class="container mx-auto">
    <div class="grid-cols-4 p-0 lg:space-y-0 lg:grid lg:gap-3">
      <div class="w-full col-span-2 my-2 row-span-2 rounded">
        <img src="/img/Painting_2.jpeg" alt="image">
      </div>
      <div class="w-full col-span-2 my-2 row-span-1 rounded">
        <img src="/img/Painting_1.jpeg" alt="image">
      </div>
      <div class="w-full rounded col-span-2 my-2 row-span-1">
        <img src="/img/Painting_3.jpeg" alt="image">
      </div>
      <div class="w-full rounded col-span-4 my-2 row-span-1">
        <img src="/img/Painting_9.png" alt="image">
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'CardHolder',
}
</script>


<style scoped>
.backdrop {
  background: url("/img/Canvas_Image.jpg");
  background-size: contain;
}
</style>
