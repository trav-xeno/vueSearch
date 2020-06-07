<template>
  <v-navigation-drawer
    v-model="drawer"
    :color="color"
    :expand-on-hover="expandOnHover"
    :mini-variant="miniVariant"
    :right="right"
    :permanent="permanent"
    :src="bg"
    absolute
    dark
  >
    <v-list dense nav class="py-0">
      <v-list-item two-line :class="miniVariant && 'px-0'">
        <v-icon>
          {{ appicon }}
        </v-icon>

        <v-list-item-content class="py-0">
          <v-list-item-title>Search Apis</v-list-item-title>
          <v-list-item-subtitle>Currently being built</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list-item v-for="item in items" :key="item.title" link>
        <v-list-item-icon>
          <v-icon>{{ item.icon }}</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title>{{ item.title }}</v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-navigation-drawer>
</template>

<script>
import { mdiViewDashboard } from "@mdi/js";
import { mdiContentSaveOutline } from "@mdi/js";
import { mdiMagnify } from "@mdi/js";

export default {
  data() {
    return {
      appicon: mdiViewDashboard,
      magnify: mdiMagnify,
      saveIcon: mdiContentSaveOutline,
      drawer: true,
      items: [
        { title: "Search", icon: mdiMagnify },
        { title: "Save", icon: mdiContentSaveOutline },
      ],
      color: "primary",
      colors: ["primary", "blue", "success", "red", "teal"],
      permanent: true,
      miniVariant: false,
      expandOnHover: true,
    };
  },
  computed: {
    bg() {
      return this.background
        ? "https://cdn.vuetifyjs.com/images/backgrounds/bg-2.jpg"
        : undefined;
    },
  },
};
</script>
