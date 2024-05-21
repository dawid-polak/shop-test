<template>
  <div style="text-align: center">
    <h1>Dog is perfect! :DD</h1>

    <router-link to="/">Home Page</router-link>

    <br />
    <hr />
    <br />

    <div v-if="dog.message">
      <img :src="dog.message" alt="dog" />
    </div>

    <div v-else>Loading...</div>
  </div>
</template>

<script setup>
const { data: dog, error } = await useFetch(
  "https://dog.ceo/api/breeds/image/random"
);
</script>

<style lang="scss" scoped></style>
