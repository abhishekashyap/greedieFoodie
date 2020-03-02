<template>
  <v-card class="mx-auto my-12 my-xs-6" max-width="374">
    <v-img height="250" :src="restraunt.image"></v-img>

    <v-card-title>{{ restraunt.name }}</v-card-title>

    <v-card-text>
      <v-row align="center" class="mx-0">
        <v-rating
          :value="4.5"
          color="amber"
          dense
          half-increments
          readonly
          size="14"
        ></v-rating>

        <div class="grey--text ml-4">4.5 (413)</div>
      </v-row>

      <div class="my-4 subtitle-1">
        $ {{ restraunt.price }} • {{ restraunt.class }}
      </div>

      <div>
        {{ restraunt.details }}
      </div>
    </v-card-text>

    <v-divider class="mx-4"></v-divider>

    <v-card-title>{{ restraunt.open }}</v-card-title>

    <v-card-text>
      <v-chip-group active-class="deep-purple accent-4 white--text" column>
        <v-chip>5:30PM</v-chip>

        <v-chip>7:30PM</v-chip>

        <v-chip>8:00PM</v-chip>

        <v-chip>9:00PM</v-chip>
      </v-chip-group>
    </v-card-text>

    <v-card-actions>
      <v-btn class="mx-2" fab dark color="pink">
        <v-icon dark>mdi-plus</v-icon>
      </v-btn>
      <v-spacer></v-spacer>
      <v-btn color="deep-purple" text>
        View menu
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  props: ["restraunt"]
};
</script>

<style></style>
