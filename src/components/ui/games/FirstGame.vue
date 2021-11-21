<template>
  <div class="card shadow bg-gray-50">
    <div class="card-body">
      <div class="grid grid-cols-2 gap-4 items-center">
        <div>
          <h2 class="card-title text-black">Catch The Trash</h2>
          <p class="leading-6 text-black">
            Catch the trash is a game to familiarize kids with waste categories. Players will pick up trash according to the selected trash bin
            (<span class="trash-organic">Organic</span>, <span class="trash-inorganic">Inorganic</span>, and <span class="trash-b3">B3</span>).
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
          <img src="../../../assets/catch.gif" class="rounded-md mx-auto" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.trash-organic{
  color: #18984C;
}

.trash-inorganic {
  color: #FBB017;
}

.trash-b3 {
  color: #ED2922;
}
</style>