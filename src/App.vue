<script>

</script>
<template>
  <div class="container mx-auto">
    <nav class="flex flex-wrap justify-center py-3 font-semibold uppercase bg-lime-800 text-white text-base">
      <router-link to="/" class="mr-2 ">Home</router-link>
      <router-link to="/about">About</router-link>

    </nav>
    <div class="text-center mt-3">

      <router-view></router-view>
    </div>
  </div>
</template>

<style></style>