<template>
  <nuxt />
</template>

<script>
export default {
  mounted() {
    document.body.style.overflow = 'hidden';
  },
  beforeDestroy() {
    document.body.style.overflow = '';
  }
}
</script>
