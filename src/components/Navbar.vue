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
  <nav ref="navbar" class="fixed top-0 left-0 w-full bg-primary-200 px-5 z-20 transition duration-200"> 
    <div class="container flex items-center justify-between h-20">
      <div class="relative z-30 flex gap-2 mb-2 lg:mb-0">
        <h1 class="text-white font-bold text-2xl">Hallow<span class="text-secondary">ee</span>nd</h1>
        <svg width="31" height="31" viewBox="0 0 31 31" fill="none" xmlns="http://www.w3.org/2000/svg">
          <path d="M8.39575 7.75016C9.64867 7.75016 10.8112 8.396 11.767 9.53266C12.4774 8.77058 13.317 8.21516 14.2083 7.94391V5.16683C14.2083 4.48169 14.4804 3.82461 14.9649 3.34014C15.4494 2.85567 16.1064 2.5835 16.7916 2.5835H19.3749V5.16683H16.7916V7.94391C17.6828 8.21516 18.5224 8.77058 19.2328 9.53266C20.1887 8.396 21.3512 7.75016 22.6041 7.75016C25.8333 7.75016 28.4166 12.0902 28.4166 17.4377C28.4166 22.7852 25.8333 27.1252 22.6041 27.1252C21.3512 27.1252 20.1887 26.4793 19.2328 25.3427C18.1866 26.4793 16.8949 27.1252 15.4999 27.1252C14.1049 27.1252 12.8133 26.4793 11.767 25.3427C10.8112 26.4793 9.64867 27.1252 8.39575 27.1252C5.16659 27.1252 2.58325 22.7852 2.58325 17.4377C2.58325 12.0902 5.16659 7.75016 8.39575 7.75016ZM11.6249 12.9168L10.0103 15.8231H13.2395L11.6249 12.9168ZM19.3749 12.9168L17.7603 15.8231H20.9895L19.3749 12.9168ZM10.3333 21.9585H12.9166L14.2083 20.6668L15.4999 21.9585H18.0833L19.3749 20.6668L20.6666 21.9585L22.6041 18.0835L17.9799 18.8843L16.7916 20.6668L15.4999 19.3752H12.9166L11.6249 20.6668L10.3333 19.3752L7.74992 18.0835L10.3333 21.9585Z" fill="white"/>
        </svg>
      </div>
      <button @click="showMenu = !showMenu" class="relative z-30 block lg:hidden text-white -mt-2 p-2">
        <svg class="w-6" viewBox="0 0 8 8"><path d="M0 1v1h8V1H0zm0 2.97v1h8v-1H0zm0 3v1h8v-1H0z" fill="currentColor"></path></svg>
      </button>
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
        <button class="px-4 lg:px-8 py-2 lg:py-3 rounded-full text-white font-bold text-lg bg-secondary w-full lg:w-auto">Donate</button>
      </div>
    </div>
  </nav>
</template>