<script setup>
import { ref } from 'vue'

definePageMeta({
  coursePage: true
})

const message = ref('Welcome to the Course Home Page!')
const testClick = () => {
  console.log('Dashboard button clicked!')
}
</script>

<template lang="pug">
.wrapper.flex.flex-col.min-h-screen.bg-white

  // Row: Main Content (sidebar assumed to be global)
  .flex.flex-row.flex-1
    .main-content.flex.flex-col.flex-1.p-10
      h2.text-3xl.font-semibold.text-customBlue.mb-6 New Page
      p.text-lg.text-gray-700.mb-4 {{ message }}
      button(
        @click="message = 'Thanks for clicking!'"
        class="px-6 py-3 bg-customBlue text-white rounded-lg shadow-md hover:bg-blue-700 transition-all duration-300"
      ) Click Me
</template>

<style scoped>
/* You can optionally style header spacing or responsiveness here */
</style>
