<template>
  <div class="card shadow bg-white">
    <div class="card-body">
      <div class="grid grid-cols-2 gap-4 items-center">
        <div>
          <h2 class="card-title">{{ selectedGame.title }}</h2>
          <p class="leading-6">
            {{ selectedGame.desc }}
          </p>
          <button
            class="
              btn btn-sm
              mt-2
              bg-blue-500
              border-blue-500
              hover:bg-blue-600
            "
          >
            Play now
          </button>
        </div>
        <div>
          <img :src="selectedImg" class="rounded-md mx-auto" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["selectedGame"],
  computed: {
    selectedImg() {
      console.log(this.selectedGame.img);
      return this.selectedGame.img;
    },
  },
};
</script>