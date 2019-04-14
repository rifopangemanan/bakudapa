<template>
  <v-app>
    <v-navigation-drawer absolute temporary="" v-model="sideNav">
      <v-list>
        <v-list-tile>
          <v-list-tile-action>
            <v-icon>streetview</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>Lia Tampa</v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
    <v-toolbar>
      <v-toolbar-side-icon
        @click.stop="sideNav = !sideNav"
        class="hidden-sm-and-up"
      ></v-toolbar-side-icon>
      <v-toolbar-title class="headline text-uppercase">
        Baku-Dapa
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-xs-only">
        <v-icon left>streetview</v-icon>
        <v-btn flat>Lia Tampa</v-btn>
      </v-toolbar-items>
    </v-toolbar>

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>
<style></style>

<script>
export default {
  name: "App",
  data() {
    return {
      //
      sideNav: false
    };
  }
};
</script>
