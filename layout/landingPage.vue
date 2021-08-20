<template>
  <v-app dark>
    <v-app-bar fixed app>
      <v-img
        class="mx-2"
        src="https://i.imgur.com/qgGY4tB.png"
        max-height="40"
        max-width="40"
        contain
      ></v-img>

      <v-toolbar-title v-text="title" />
    </v-app-bar>
    <v-main>
      <!-- <v-container> -->
      <nuxt />
      <SnackBar />
      <!-- </v-container> -->
    </v-main>
  </v-app>
</template>
<script>
export default {
  data() {
    return {
      title: "Lighthouse Learning Management System"
    };
  }
};
</script>
