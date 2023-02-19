<template>
  <div class="text-3xl font-bold text-center py-16">
    <h2 class="one">Nuxt 3</h2>
    <p class="text-gray-400">+</p>
    <h2 class="two">Tailwind CSS</h2>
    <p class="text-gray-400">+</p>
    <h2 class="three">GSAP</h2>
    <button class="p-3 mt-6 bg-black text-white" @click="clickAnimations">Animate</button>
  </div>
</template>
  
<script>
  import gsap from 'gsap'
  
  export default {
    mounted: function() {
      this.startAnimations()
    },
    methods: {
      startAnimations: function() {
        gsap.to('.one', { rotation: 360, duration: 1, ease: "bounce.out" }),
        gsap.to('.two', { rotation: 360, duration: 1, delay: 0.5, ease: "bounce.out" }),
        gsap.to('.three', { rotation: 360, duration: 1, delay: 1, ease: "bounce.out" })
      },
      clickAnimations: function() {
        gsap.to('.one', { rotation: 0, duration: 1, ease: "bounce.out" }),
        gsap.to('.two', { rotation: 0, duration: 1, delay: 0.5, ease: "bounce.out" }),
        gsap.to('.three', { rotation: 0, duration: 1, delay: 1, ease: "bounce.out" })
      }
    }
  }
</script>