<template>
  <main class="container">
    <AppHeader />
    <AppRestuarantInfo :datasource="fooddata" />
  </main>
</template>

<script>
import { mapState } from "vuex";
import AppHeader from "@/components/AppHeader.vue";
import AppRestuarantInfo from "@/components/AppRestuarantInfo.vue";

export default {
  components: {
    AppRestuarantInfo,
    AppHeader,
  },
  computed: {
    ...mapState(["fooddata"]),
  },
};
</script>
