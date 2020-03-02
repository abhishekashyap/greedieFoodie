<template>
  <v-app id="foodie">
    <v-app-bar app clipped-left class="primary">
      <v-app-bar-nav-icon @click="drawer = !drawer" />
      <span class="title ml-3 mr-5">
        Greedie&nbsp;
        <span class="font-weight-light">Foodie</span>
      </span>
      <v-text-field
        solo-inverted
        flat
        hide-details
        label="Search"
        prepend-inner-icon="search"
      />
      <v-spacer />
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app clipped color="grey lighten-4">
      <v-list dense class="grey lighten-4">
        <template v-for="(item, i) in items">
          <v-row v-if="item.heading" :key="i" align="center">
            <v-col cols="6">
              <v-subheader v-if="item.heading">{{ item.heading }}</v-subheader>
            </v-col>
            <v-col cols="6" class="text-right">
              <v-btn small text>edit</v-btn>
            </v-col>
          </v-row>
          <v-divider v-else-if="item.divider" :key="i" dark class="my-4" />
          <v-list-item v-else :key="i" link>
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title class="grey--text">{{
                item.text
              }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </template>
      </v-list>
    </v-navigation-drawer>

    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
export default {
  props: {
    source: String
  },
  data: () => ({
    drawer: null,
    items: [
      { icon: "lightbulb_outline", text: "What's popular" },
      { icon: "touch_app", text: "View orders" },
      { divider: true },
      { heading: "My Account" },
      { icon: "home", text: "Manage addresses" },
      { icon: "shopping_cart", text: "View cart" },
      { divider: true },
      { icon: "settings", text: "Settings" },
      { icon: "phonelink", text: "Download mobile app" },
      { icon: "help", text: "Help" },
      { divider: true },
      { text: "Seller" },
      { text: "Buyer" }
    ]
  })
};
</script>

<style>
#foodie .v-navigation-drawer__border {
  display: none;
}
</style>
