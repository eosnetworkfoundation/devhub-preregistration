<template>
  <section class="generic-header">
    <section class="inner-container">

      <section class="slot-container">
        <slot />
      </section>
    </section>
  </section>
</template>

<script>
  export default {
  }
</script>

<style lang="scss" scoped>
  .generic-header {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    width:100%;
    position: relative;
    background:#fff;
    border-bottom:1px solid rgba(0,0,0,0.1);

    .inner-container {
      max-width:900px;
      margin:0 auto;
      text-align: center;
      padding:0 30px;

      h3 {
        margin-top:10px;
      }

      p {
        margin: 50px auto 0;
        max-width:700px;
      }
    }


    .slot-container {
      display:flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }

  }
</style>
