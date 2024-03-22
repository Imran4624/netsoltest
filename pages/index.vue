<template>
  <div class="mainContainer">
    <h4 class="newsInsight">News And Insights</h4>
    <div class="titleContainer">
      <h1 class="title">Latest Insights from Leading Voices</h1>
      <p class="desc">
        Solving the world’s problems through technology wouldn’t be possible
        without our most important invention: the NetSol. Have a look at our
        talented teams.
      </p>
    </div>
    <a class="viewAll" href="/">View all</a>
    <div class="cardLis" style="display:flex;flex-wrap: wrap ; justify-content:center;align-items:center " >
      <div class="cardListItem" v-for="product in products" :key="product.id">
        <CardView :product="product" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import CardView from "~/components/CardView.vue";
const country = ref("")
const products = [
   {
          id: 1,
          imageUrl: "/img1.png",
          type: "News",
          title: "Leasing Life Conference & Awards",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 2,
          imageUrl: "/img2.png",
          type: "Blog",
          title: "Auto Finance Summit 2023",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 3,
          imageUrl: "/img3.png",
          type: "Blog",
          title: "Careers at Netsol",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
        {
          id: 4,
          imageUrl: "/img4.png",
          type: "News",
          title: "Leasing Life Conference & Awards",
          description:
            "Solving the world’s problems through technology wouldn’t be possible without our most important invention.",
        },
];
</script>

<style scoped>
.mainContainer {
  display: flex;
  flex-direction: column;
  margin: 0px;
  padding: 0px;
  justify-content: center;
  align-items: center;
width: 100%;
}
.newsInsight {
  background: linear-gradient(89.97deg, #030a2d -0.5%, #030616 99.97%);
  color: white;
  text-align: center;
  width: 181px;
  padding: 10px 20px;
margin: 10px 0px;
  border-radius: 100px;
  font-size: 22px;
  font-weight: 500;
}
.titleContainer {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.title {
  color: white;
  font-size: 56px;
font-weight: 500;
padding: 0;
margin: 0;
}
.desc {
  color: #ffffffb8;
  font-size: 22px;
  width: 1108px;
  text-align: center;
}
.viewAll {
  color: white;
  font-size: 16px;
  font-weight: 500;
padding: 0;
margin: 0;
}
.cardList {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around; /* Adjust as needed */
}

.cardListItem {
  flex: 0 0 auto; /* Prevent items from stretching */
  margin: 10px;
}
</style>
