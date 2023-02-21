<script setup>
import { ref } from "vue";
let options = ref([
  {
    name: "Home",
  },
  {
    name: "Services",
  },
  {
    name: "About",
    children: [
      {
        name: "About Us",
      },
      {
        name: "Testimonials",
      },
      {
        name: "FAQ's",
      },
    ],
  },
  {
    name: "Jobs",
  },
  {
    name: "Contact",
    children: [
      {
        name: "Upload",
      },
    ],
  },
  {
    name: "News",
  },
]);
</script>


<template>
  <div id="container">
    <div class="nav-bar">
      <ul>
        <li class="menu-items dropdown" v-for="item in options">
          {{ item.name }}
        </li>
      </ul>
    </div>
  </div>
</template>


<style lang="css" scoped>
li.menu-items {
  color: white;
  list-style-type: none;
  display: inline;
  padding-right: 5%;
}

#container .nav-bar {
  padding: 5% 5% 10% 5%;
  background-color: black;
}
</style>