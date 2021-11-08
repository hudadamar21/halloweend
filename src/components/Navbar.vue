<script setup>
import { onMounted, ref } from "vue";

const navbar = ref('')
const showMenu = ref(false)

onMounted(() => {
  window.onscroll = () => {
  if(window.scrollY === 0) {
    navbar.value.classList.remove('bg-primary-200')
  } else {
    navbar.value.classList.add('bg-primary-200')
  }
}
})
</script>

<template>
  <nav ref="navbar" class="fixed top-0 left-0 w-full bg-primary-200 z-20 transition duration-200"> 
    <div class="container flex items-center justify-between h-20">
      <div class="relative z-30 flex items-center gap-2 mb-2 lg:mb-0">
        <h1 class="text-white font-bold text-lg lg:text-2xl">Hallow<span class="text-secondary">ee</span>nd</h1>
        <svg class="w-7 lg:w-9" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8.39575 7.75016C9.64867 7.75016 10.8112 8.396 11.767 9.53266C12.4774 8.77058 13.317 8.21516 14.2083 7.94391V5.16683C14.2083 4.48169 14.4804 3.82461 14.9649 3.34014C15.4494 2.85567 16.1064 2.5835 16.7916 2.5835H19.3749V5.16683H16.7916V7.94391C17.6828 8.21516 18.5224 8.77058 19.2328 9.53266C20.1887 8.396 21.3512 7.75016 22.6041 7.75016C25.8333 7.75016 28.4166 12.0902 28.4166 17.4377C28.4166 22.7852 25.8333 27.1252 22.6041 27.1252C21.3512 27.1252 20.1887 26.4793 19.2328 25.3427C18.1866 26.4793 16.8949 27.1252 15.4999 27.1252C14.1049 27.1252 12.8133 26.4793 11.767 25.3427C10.8112 26.4793 9.64867 27.1252 8.39575 27.1252C5.16659 27.1252 2.58325 22.7852 2.58325 17.4377C2.58325 12.0902 5.16659 7.75016 8.39575 7.75016ZM11.6249 12.9168L10.0103 15.8231H13.2395L11.6249 12.9168ZM19.3749 12.9168L17.7603 15.8231H20.9895L19.3749 12.9168ZM10.3333 21.9585H12.9166L14.2083 20.6668L15.4999 21.9585H18.0833L19.3749 20.6668L20.6666 21.9585L22.6041 18.0835L17.9799 18.8843L16.7916 20.6668L15.4999 19.3752H12.9166L11.6249 20.6668L10.3333 19.3752L7.74992 18.0835L10.3333 21.9585Z" fill="white"/>
        </svg>
      </div>
      <div class="flex lg:hidden items-center gap-2">
        <button class="relative z-30 px-4 py-2 -mt-1.5 text-sm rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Donate</button>
        <button @click="showMenu = !showMenu" class="relative z-30 text-white -mt-2 p-2">
          <svg width="18" height="12" viewBox="0 0 18 12" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M1 12H17C17.55 12 18 11.55 18 11C18 10.45 17.55 10 17 10H1C0.45 10 0 10.45 0 11C0 11.55 0.45 12 1 12ZM1 7H17C17.55 7 18 6.55 18 6C18 5.45 17.55 5 17 5H1C0.45 5 0 5.45 0 6C0 6.55 0.45 7 1 7ZM0 1C0 1.55 0.45 2 1 2H17C17.55 2 18 1.55 18 1C18 0.45 17.55 0 17 0H1C0.45 0 0 0.45 0 1Z" fill="white"/>
          </svg>
        </button>
      </div>
      <div
        class="
          absolute lg:static top-20 inset-x-0
          flex flex-col lg:flex-row items-center gap-5 lg:gap-10
          bg-primary-200 lg:bg-transparent pt-5 pb-10 px-5 lg:p-0
          transition duration-500 lg:duration-200 lg:-translate-y-0
        "
        :class="!showMenu ? 'translate-y-[-150%]' : '-translate-y-0'"
      >
        <a @click="showMenu = false" class="text-white font-medium" href="#home">Home</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#category">Category</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#about">About</a>
        <a @click="showMenu = false" class="text-white font-medium" href="#trick-or-treat">Trick or Treat</a>
        <button class="hidden md:block px-8 py-3 rounded-full text-white font-medium tracking-wider uppercase bg-secondary w-full lg:w-auto">Donate</button>
      </div>
    </div>
  </nav>
</template>