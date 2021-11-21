<template>
  <div class="grid grid-rows-none justify-items-center mx-auto w-full">
    <div>
      <div class="btn-group">
        <button
          class="
            btn
            border-green-300
            hover:bg-green-400 hover:border-green-300 hover:text-white
          "
          @click="setSelectedComponent('first-game')"
          :class="{
            'bg-green-700': selectedComponent == 'first-game',
            'text-white': selectedComponent == 'first-game',
            'text-green-500': selectedComponent !== 'first-game',
            'bg-white': selectedComponent !== 'first-game',
          }"
        >
          Catch the trash
        </button>
        <button
          class="
            btn
            border-green-300
            hover:bg-green-400 hover:border-green-300 hover:text-white
          "
          @click="setSelectedComponent('second-game')"
          :class="{
            'bg-green-700': selectedComponent == 'second-game',
            'text-white': selectedComponent == 'second-game',
            'text-green-500': selectedComponent !== 'second-game',
            'bg-white': selectedComponent !== 'second-game',
          }"
        >
          Super Trash Picker
        </button>
         <button
          class="
            btn
            border-green-300
            hover:bg-green-400 hover:border-green-300 hover:text-white
          "
          @click="setSelectedComponent('third-game')"
          :class="{
            'bg-green-700': selectedComponent == 'third-game',
            'text-white': selectedComponent == 'third-game',
            'text-green-500': selectedComponent !== 'third-game',
            'bg-white': selectedComponent !== 'third-game',
          }"
        >
          Hay Day
        </button>
      </div>
    </div>
    <div class="mt-5 w-auto">
      <transition name="card" mode="out-in">
          <component :is="selectedComponent"></component>
        <!-- <game-card :selectedGame="selectedGame"></game-card> -->
      </transition>
    </div>
  </div>
</template>

<script>
import FirstGame from "../ui/games/FirstGame.vue";
import SecondGame from "../ui/games/SecondGame.vue";
import ThirdGame from "../ui/games/ThirdGame.vue";

export default {
  components: {
    "first-game": FirstGame,
    "second-game": SecondGame,
    "third-game": ThirdGame,
  },
  data() {
    return {
      selectedComponent: "first-game",
    };
  },
  methods: {
    setSelectedComponent(cmp) {
      this.selectedComponent = cmp;
    },
  },
};
</script>

<style scoped>
.card-enter-active {
  animation: card 0.3s ease-in;
}

.card-leave-active{
  animation: card 0.3s ease-out reverse;
}

@keyframes card {
  from {
    opacity: 0;
    transform: scale(0.8);
  }
  to {
    opacity: 1;
    transform: scale(1);
  }
}
</style>