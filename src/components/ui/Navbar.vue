<template>
  <div class="navbar mb-2 bg-transparent text-black sticky top-0 z-10">
    <div class="flex-none px-2 mx-2">
      <span class="text-lg font-bold">CLEAN HERO</span>
    </div>
    <div class="flex-1 px-2 mx-2 justify-end">
      <div class="items-stretch hidden lg:flex">
        <a
          class="
            btn btn-ghost btn-sm
            rounded-btn
            font-normal
            hover:bg-green-400 hover:text-white
          "
          ref="link"
          href="#home"
          @click="smoothScroll"
        >
          Home
        </a>
        <a
          class="
            btn btn-ghost btn-sm
            rounded-btn
            font-normal
            hover:bg-green-400 hover:text-white
          "
          ref="link"
          href="#games"
          @click="smoothScroll"
        >
          Games
        </a>
        <a
          class="
            btn btn-ghost btn-sm
            rounded-btn
            font-normal
            hover:bg-green-400 hover:text-white
          "
          ref="link"
          href="#about"
          @click="smoothScroll"
        >
          About
        </a>
        <a
          class="
            btn btn-ghost btn-sm
            rounded-btn
            font-normal
            hover:bg-green-400 hover:text-white
          "
          ref="link"
          href="#contact"
          @click="smoothScroll"
        >
          Contact
        </a>
      </div>
    </div>
  </div>
</template>