<template>
  <v-carousel cycle height="400" hide-delimiter-background show-arrows-on-hover>
    <v-carousel-item v-for="(slide, i) in slides" :key="i">
      <v-img :src="slide.image" height="100%">
        <v-row class="fill-height" align="center" justify="center">
          <div class="display-3 white--text text-center">
            {{ slide.name }}
          </div>
        </v-row>
      </v-img>
    </v-carousel-item>
  </v-carousel>
</template>
<script>
export default {
  data() {
    return {
      colors: [
        "indigo",
        "warning",
        "pink darken-2",
        "red lighten-1",
        "deep-purple accent-4",
      ],
      slides: [
        {
          name: "Restaurant on web",
          image:
            "https://images.unsplash.com/photo-1550353127-b0da3aeaa0ca?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1351&q=80",
        },
        {
          name: "Veggies friendly restaurant",
          image:
            "https://images.unsplash.com/photo-1549834146-0702b38f1bed?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80",
        },
        {
          name: "On time, or it is on us",
          image:
            "https://images.unsplash.com/photo-1553851935-cad21b77d358?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1355&q=80",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
v-img {
  filter: blur(5px);
}
</style>
