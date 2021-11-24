<template>
<section class="max-w-6xl mx-auto px-4 sm:px-6 lg:px-4 py-12">
    <div class="text-center pb-12">

        <h1 class="font-bold text-3xl md:text-4xl lg:text-5xl font-heading text-gray-900">
            Artikel Terbaru
        </h1>
    </div>
    <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div v-for="post in posts" :key="post.id" class="w-full bg-white rounded-lg sahdow-lg overflow-hidden flex flex-col justify-center items-center">
            <div>
                <img class="object-center object-cover h-auto w-full" :src="post.image" alt="photo">
            </div>
            <div class="text-center py-8 sm:py-6">
                <p class="text-xl text-gray-700 font-bold mb-2">{{ post.title }}</p>
                <p class="text-base text-gray-400 font-normal">{{ post.category }}</p>
            </div>
        </div>
    </div>
</section>

</template>

<script>
import axios from "axios";
export default {
  data() {
    return {
      posts: "",
    };
  },
  created() {
    axios
      .get("https://fakestoreapi.com/products?limit=10")
      .then((response) => {
        console.log(response);
        this.posts = response.data;
      });
  },
};
</script>
