<script setup>
import { ref } from "vue";

const items = ref(["one", "two", "three"]);

const stuff = () => {};
</script>

<template>
  <div id="container">
    <div>
      <vue3-simple-typeahead
        id="typeahead_id1"
        class="input left"
        placeholder="1Start writing..."
        :items="items"
        :minInputLength="1"
      >
      </vue3-simple-typeahead>
    </div>
    <div>
      <vue3-simple-typeahead
        id="typeahead_id2"
        class="input right"
        placeholder="2Start writing..."
        :items="items"
        :minInputLength="1"
      >
      </vue3-simple-typeahead>
    </div>
  </div>
  <div id="btn" @click="stuff">
    <button>Enter</button>
  </div>
</template>

<style scoped>
#container {
  display: flex; /* establish flex container */
  flex-direction: row; /* stack flex items vertically */
  justify-content: center; /* center items vertically, in this case */
  align-items: center; /* center items horizontally, in this case */
  padding-top: 1%;
  padding-bottom: 10%;
}
#btn {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
