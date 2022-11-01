<template>
  <!-- <Tutorial/> -->
  <div>
    <Hero />
    <LargeCardDisplay 
      v-for="cardInfo in largeCardInfo"
      :key="cardInfo.id"
      :cardSection="cardInfo"
    />
  </div>
</template>

<script>
// This is how you do imports in NUXT where the @ denotes the root directory
import { largeCardSections } from '@/assets/data.js'
export default {
    name: "IndexPage",
    data: () => ({
      // fetching data from the data.js. There, data is being exported as LargeCardSections hence the name
        largeCardInfo: largeCardSections
    }),
}
</script>
