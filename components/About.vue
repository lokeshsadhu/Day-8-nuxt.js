<!-- About.vue -->
<template>
<div class="about-page">
    <div class="container mx-auto p-8">
    <h1 class="text-3xl font-bold mb-4 color">About Us</h1>
    <p>
        Welcome to our about page! We are a team of passionate individuals dedicated to providing high-quality services. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Quisque auctor gravida turpis, id ultrices quam tincidunt vel. Suspendisse potenti.
    </p>
    <h1 class="text-3xl font-bold mb-4 color">Technologies we work on</h1>
    <ul v-for="i in softwareTechnologies">
        <li>{{ i }}</li>
    </ul>
    </div>
</div>
</template>

<script setup>
const softwareTechnologies = [
  'JavaScript',
  'Python',
  'Java',
  'React',
  'Node.js',
  'Django',
  'C#',
  'Vue.js',
];
</script>

<style scoped>
.about-page {
background: linear-gradient(to right,  #071e26, #22c55e);
display: flex;
justify-content: center;
align-items: center;
color: #071e26; 
}
</style>
