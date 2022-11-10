<template>
  <main class="container restaurant">
    <div class="restaurantheading">
      <h1>Restaurants</h1>

      <AppSelect @change="selectedRestaurant = $event" />
    </div>
    <AppRestuarantInfo :datasource="filteredRestaurants" />
  </main>
</template>

<script>
import { mapState } from "vuex";
import AppRestuarantInfo from "@/components/AppRestuarantInfo.vue";
import AppSelect from "@/components/AppSelect.vue";

export default {
  components: {
    AppSelect,
    AppRestuarantInfo,
  },
  data() {
    return {
      selectedRestaurant: "",
    };
  },
  computed: {
    ...mapState(["fooddata"]),
    filteredRestaurants() {
      if (this.selectedRestaurant) {
        return this.fooddata.filter((el) => {
          const name = el.name.toLowerCase();
          return name.includes(this.selectedRestaurant);
        });
      } else {
        return this.fooddata;
      }
    },
  },
};
</script>
