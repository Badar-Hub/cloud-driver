<template>
  <q-layout view="lHh Lpr lFf">
    <q-page-container>
      <HomePage />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";
import HomePage from "./components/HomePage.vue";

export default {
  name: "LayoutDefault",

  components: {
    HomePage,
  },

  setup() {
    return {
      leftDrawerOpen: ref(false),
    };
  },
};
</script>
