<template>
  <section class="image">
    <div
      v-for="menuitem in store.menu"
      :key="menuitem.id"
      :style="`background: url(/${menuitem.img}) no-repeat center center`"
      class="items"
    ></div>
  </section>
</template>

<script>
export default {
  props: {
    datasource: {
      type: [Array, Object],
    },
  },
};
</script>

<style lang="scss" scoped></style>
