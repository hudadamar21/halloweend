<template>
  <div class="relative my-32 bg-gradient-to-b from-primary-200/30 to-primary-100/10 pb-10 md:pb-32 rounded-lg">
    <div class="p-10">
      <h2 class="text-6xl font-bold text-white mb-4">Subscribe</h2>
      <p class="text-lg text-white">Subcribe to our newsletters and stay update!</p> 
      <form action="#" class="mt-12">
        <div class="h-20 w-1/2 flex items-center">
          <input 
            class="h-full flex-grow rounded-l-lg px-6 text-lg" 
            type="text" 
            placeholder="Enter your email address"
          />
          <button class="h-full px-6 text-white font-bold bg-secondary rounded-r-lg">SUBSCRIBE</button>
        </div>
      </form>
    </div>
    <div class="absolute right-10 bottom-10 w-1/3 hidden md:block">
      <img src="../assets/images/about-img.webp" alt="">
    </div>
  </div>
</template>