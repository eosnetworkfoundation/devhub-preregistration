<template>
  <section>
    <Nav />
    <section class="page-body">
      <Nuxt />
    </section>
    <Footer />
  </section>
</template>

<script>
export default {
  head() {
    return {
      title: "EOS - Learn "
    };
  },
}
</script>

<style lang="scss" scoped>
  .page-body {
    min-height: 50vh;
  }
</style>
