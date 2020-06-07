<template>
  <v-app>
    <v-app-bar app color="primary" dark>
      <div class="d-flex align-center">
        <span class="mr-2 text-center">Vue Search App</span>
      </div>
    </v-app-bar>

    <v-content>
      <Nav />
      <HelloWorld />
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from "./components/HelloWorld";
import Nav from "./components/Nav";
export default {
  name: "App",

  components: {
    HelloWorld,
    Nav,
  },

  data: () => ({
    //
  }),
};
</script>
