<template>
  <main class="main">
    <the-navigation />
    <nuxt />
    <the-footer />
  </main>
</template>

<script>
export default {
  data() {
    return {
      vhTimer: null,
    }
  },

  mounted() {
    this.setVHUnit()
    window.addEventListener('resize', this.setVHUnit)
  },

  destroyed() {
    window.removeEventListener('resize', this.setVHUnit)
    document.documentElement.style.removeProperty('--vh')
  },

  methods: {
    setVHUnit() {
      clearTimeout(this.vhTimer)
      const vh = window.innerHeight * 0.01
      document.documentElement.style.setProperty('--vh', `${vh}px`)
    },
  },
}
</script>
