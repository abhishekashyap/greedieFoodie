<template>
  <v-container fluid class="grey lighten-4 fill-height">
    <v-row justify="center" align="center">
      <appCarousel></appCarousel>
    </v-row>
    <v-row justify="center" align="center">
      <appCard
        v-for="(restraunt, index) in restraunts"
        :key="index"
        :restraunt="restraunt"
      ></appCard>
    </v-row>
  </v-container>
</template>

<script>
import appCard from "@/components/Card.vue";
import appCarousel from "@/components/Carousel.vue";

export default {
  components: {
    appCard: appCard,
    appCarousel: appCarousel
  },
  data() {
    return {
      restraunts: [
        {
          image:
            "https://images.unsplash.com/photo-1482049016688-2d3e1b311543?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=653&q=80",
          name: "Square one",
          class: "Canteen",
          details: "Multifloor cafe with seating upto 50",
          open: "9AM - 11PM",
          price: "20 - 700"
        },
        {
          image:
            "https://images.unsplash.com/photo-1506354666786-959d6d497f1a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1950&q=80",
          name: "Dominos pizza",
          class: "Pizza",
          details: "Takeaway",
          open: "11AM - 1AM",
          price: "150 - 2500"
        },
        {
          image:
            "https://images.unsplash.com/photo-1509042239860-f550ce710b93?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80",
          name: "Cafe Coffee Day",
          class: "Cafe",
          details: "Specialized in coffee based items.",
          open: "9AM - 9PM",
          price: "20 - 1500"
        },
        {
          image:
            "https://images.unsplash.com/photo-1517984055083-fd6e1e788e54?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80",
          name: "Kentucky Fried Chicken",
          class: "Non-veg",
          details: "Specializes in non-veg food. Seating for upto 100.",
          open: "9AM - 10PM",
          price: "200 - 3500"
        }
      ]
    };
  }
};
</script>
