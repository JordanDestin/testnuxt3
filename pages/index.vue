<script setup>
const { data: categories } = await useFetch("http://localhost:8000/api/categories");

console.log(categories);
</script>

<template>
  <div
    class="hero min-h-screen"
    style="background-image: url(https://placeimg.com/1000/800/arch)"
  >
    <div class="hero-overlay bg-opacity-60"></div>
    <div class="hero-content text-center text-neutral-content">
      <div class="max-w-md">
        <h1 class="mb-5 text-5xl font-bold">Hello there</h1>
        <p class="mb-5">
          Provident cupiditate voluptatem et in. Quaerat fugiat ut assumenda excepturi
          exercitationem quasi. In deleniti eaque aut repudiandae et a id nisi.
        </p>
        <button class="btn btn-primary">Get Started</button>
      </div>
    </div>
  </div>
  <div class="w-full text-center">
    <ul class="menu menu-horizontal bg-base-100 rounded-box">
      <li v-for="category in categories.data" :key="category.id">
        <NuxtLink :to="{ path: 'category/' + category.id }">
          {{ category.name }}
        </NuxtLink>
      </li>

    </ul>
  </div>

  <div class="mt-8 container w-full max-w-5xl mx-auto">
    <productAllProducts />
  </div>
</template>
