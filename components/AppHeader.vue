<template>
  <section class="masthead" role="img" aria-label="Image Description">
    <h1>Nuxt Food App</h1>
    <button>See restaurants</button>
  </section>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.masthead {
  width: 100%;
  height: 70vh; /* if you don't want it to take up the full screen, reduce this number */
  padding: 1px;
  overflow: hidden;
  background-size: cover !important;
  background: linear-gradient(
      to bottom,
      rgba(0, 0, 0, 0) 0%,
      rgba(0, 0, 0, 0) 80%,
      rgba(0, 0, 0, 0.65) 100%
    ),
    url("~assets/headerimg.jpg") no-repeat center center scroll;
}

h1 {
  font-style: normal;
  font-weight: bold;
  color: #eee;
  font-size: 8vmin;
  letter-spacing: 0.03em;
  line-height: 1;
  text-shadow: 1px 2px 4px rgba(0, 0, 0, 0.8);
  margin-bottom: 36px;
}
</style>
