<template>
    <div class="counter">
        <h1>Counter</h1>
        <h2 class="font-bold">{{ count }}</h2>
        <div>
        <button @click="count++" type="button" class="focus:outline-none text-white bg-green-700 hover:bg-green-800 focus:ring-4 focus:ring-green-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-green-600 dark:hover:bg-green-700 dark:focus:ring-green-800">Increase</button>
        <button @click="count--" type="button" class="focus:outline-none text-white bg-red-700 hover:bg-red-800 focus:ring-4 focus:ring-red-300 font-medium rounded-lg text-sm px-5 py-2.5 me-2 mb-2 dark:bg-red-600 dark:hover:bg-red-700 dark:focus:ring-red-900">Decrease</button>
        </div>
    </div>
</template>

<script setup>
const count=ref(0)
</script>

<style scoped>
.counter{
background: linear-gradient(to right,  #071e26, #22c55e);
display: flex;
flex-direction: column;
justify-content: center;
align-items: center;
color: #071e26; 
}
</style>
