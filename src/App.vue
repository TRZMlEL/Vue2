<template>
  <main class="flex items-center justify-center w-screen h-screen bg-neutral-900 flex-col gap-6">

    <h1 v-if="likes > 0" class="text-green-700 text-2xl">
      This website have {{ likes }} 👍
    </h1>

    <h1 v-else="likes > 0" class="text-green-700 text-2xl">
      Nobody like it 😢
    </h1>

    <button v-on:click="like()" class="bg-green-700 rounded-lg w-30 h-10 shadow-lg p-3 flex items-center justify-center">
      👍 I Like it 👍
    </button>
  </main>
</template>

<script>
  export default {

    data() {
      return{
        likes: 0,
      }
    },

    methods: {
      like() {
        this.likes++;
      }
    }
  }
</script>
