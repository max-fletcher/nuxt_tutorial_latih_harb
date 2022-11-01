<template>
   <div class="card">
      <!-- NUXT's way of importing files. @ is for the root directory. From there, you go to assets, then to images and find your respective 
         image. If that image is not found, then show fe1.jpg -->
      <img :src="require(`@/assets/images/${card.image || 'fe1.jpg'}`)" alt="fe" class="image">
      <h3 class="header">{{ card.title }}</h3>
      <p class="snippet">{{ card.snippet }}</p>
   </div>
</template>

<script>
   export default {
      props: ['card']
   }
</script>

<style scoped>
   .card {
      width: 31.5%;
      height: 25rem;
      border: none;
      overflow: hidden;
      padding: 0;
      cursor: pointer;
   }
   .image {
      height: 65%;
      border-radius: 0.5rem;
   }
   .header {
      font-size: 1.15rem;
      margin-top: 0.4rem;
   }
   .snippet {
      color: grey
   }
</style>