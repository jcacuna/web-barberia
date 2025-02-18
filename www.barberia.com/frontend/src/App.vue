<script setup>
import { RouterLink, RouterView } from 'vue-router'
import { ref, onMounted, onUnmounted } from 'vue'

const images = [
  "/img/1.jpg",
  "/img/2.jpg",
  "/img/3.png"
]

const currentImage = ref(images[0])
let interval = null

onMounted(() => {
  let index = 0
  interval = setInterval(() => {
    index = (index + 1) % images.length
    currentImage.value = images[index]
  }, 3000) // Cambia cada 3 segundos
})

onUnmounted(() => {
  clearInterval(interval)
})
</script>

<template>
  <div class="md:flex h-screen">
    <!-- Fondo dinámico -->
    <div class="h-64 md:h-auto bg-cover bg-center md:w-1/3 transition-all duration-500"
      :style="{ backgroundImage: `url(${currentImage})` }"></div>

    <!-- Contenido -->
    <div class="md:w-2/3 px-10 py-5 min-h-full overflow-y-scroll">
      <RouterView />
    </div>
  </div>
</template>
