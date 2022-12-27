<template>
    <div class="text-3xl font-bold text-center py-16">
      <h2 class="one">Nuxt 3</h2>
      <p class="text-gray-400">+</p>
      <h2 class="two">Tailwind CSS</h2>
      <p class="text-gray-400">+</p>
      <h2 class="three">GSAP</h2>
    </div>
  </template>
  
  <script setup>
  import gsap from 'gsap';
  
  onMounted(() => {
    gsap.to('.one', { rotation: 360, duration: 1, ease: "bounce.out" }),
    gsap.to('.two', { rotation: 360, duration: 1, delay: 0.5, ease: "bounce.out" }),
    gsap.to('.three', { rotation: 360, duration: 1, delay: 1, ease: "bounce.out" })
  });
  
  </script>