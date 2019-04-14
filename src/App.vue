<template>
  <v-app dark>
    <v-navigation-drawer absolute temporary="" v-model="sideNav">
      <v-list>
        <v-list-tile v-for="item in menuItems" :key="item.title">
          <v-list-tile-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>{{ item.title }}</v-list-tile-content>
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
        <v-btn flat v-for="item in menuItems" :key="item.title">
          <v-icon left dark="">{{ item.icon }}</v-icon>
          {{ item.title }}
        </v-btn>
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
      sideNav: false,
      menuItems: [
        { icon: "streetview", title: "Lia Tampa" },
        { icon: "room", title: "Ator Tampa" },
        { icon: "person", title: "Profil" },
        { icon: "face", title: "Daftar" },
        { icon: "lock_open", title: "Maso" }
      ]
    };
  }
};
</script>
