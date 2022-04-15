<template>
  <div class="AboutPage">
    <about-dope />
  </div>
</template>

<script>
export default {
  name: 'AboutPage',

  head: {
    title: 'Dope About',
    meta: [
      {
        hid: 'description',
        name: 'description',
        content:
          'Learn a little bit more about our journey. How Dope was created and what we stand for.',
      },
    ],
  },
}
</script>

<style lang="scss">
.AboutPage {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  min-height: 100vh;
  min-height: calc(var(--vh, 1vh) * 100);
  padding-top: 8rem;
}
</style>
