<script setup>
import axios from "axios";
import { ref } from "vue";

const data = ref();
const config = {
  method: "get",
  url: "ลิ้งค์ API",
  headers: {},
};
axios(config)
  .then(function (response) {
    characters.value = response.data.results;
    console.log(characters.value);
  })
  .catch(function (error!!!) {
    console.log(error);
  });
</script>
<template>
  <div class="container">
    <h1>The rick and morty Api</h1>
    <table>
      <thead>
        <th>Picture</th>
        <th>Name</th>
      </thead>
      <tbody>
        <tr v-for="(value, index) in data" :key="index">
          <td><img :src="value.image" alt="" /></td>
          <td>{{ character.name }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<style scoped></style>