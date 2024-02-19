<template>
  <div class="text-center">
    <nav class="bg-gray-800 p-4">
      <div class="container mx-auto flex justify-between items-center">
        <div class="text-white font-bold text-lg"><img class="image" src="https://cp.drunomics.com/files/styles/bounding_box_1600x1000/public/2022-12/icon-green-square.png?itok=9VmSTOtM"/></div>
        <div>
          <ul class="flex space-x-4">
            <li><a href="#" @click="view('welcome')" class="text-white hover:text-gray-300">Home</a></li>
            <li><a href="#" @click="view('counter')" class="text-white hover:text-gray-300">Counter</a></li>
            <li><a href="#" @click="view('about')" class="text-white hover:text-gray-300">About</a></li>
          </ul>
        </div>
      </div>
    </nav>
    <!-- <button @click="toggle" class="bg-blue-500 text-white px-4 py-2 rounded">Toggle</button> -->
    <!-- <component :is="MyComponent"/> -->
    <LazyHomeWelcome v-if="page==='welcome'" />
    <LazyCounter v-if="page==='counter'" />
    <LazyAbout v-if="page==='about'"/>
    <NuxtLayout>
      <NuxtPage/>
    </NuxtLayout>
  </div>
  
</template>

<script setup>
// const MyComponent=shallowRef(resolveComponent("Counter"))
const page=ref('welcome')

const view=(name)=>{
  page.value=name
}
</script>

<style scoped>
.image{
  height: 45px;
  width: 70px;
}
</style>