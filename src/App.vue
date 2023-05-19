<script setup lang="ts">
import CardList from './components/CardList.vue';

const items = [{
  id: 1,
  title: 'Photography',
  options: ["Drone Photography", "Interiors", "Exteriors / Architectural"],
  description: 'Every photograph we produce finds the beauty in your property while serving as a profitable asset.',
  img: "https://picsum.photos/200/350"
},
{
  id: 2,
  title: 'Virtual Staging',
  description: ['Our staging will help you sell the potential of your space.',
    'We can work off of our own photography or photos you provide.'],
  img: "https://picsum.photos/200/350"
},
{
  id: 3,
  title: 'Renderings',
  options: ["Interiors", "Exteriors"],
  description: "Renderings are the gold standard in pre-construction marketing.",
  img: "https://picsum.photos/200/350"
},
{
  id: 4,
  title: 'Interactive Tours',
  options: ["Matterport",
    "Video Walkthroughs"],
  description: "Give your audience the ability to explore your property without requiring in-person travel.",
  img: "https://picsum.photos/200/350"
},
{
  id: 5,
  title: 'Floor Plans',
  options: ["On-site Measure 2D", "Floor Plans 3D", "Floor Plans"],
  description: "We produce laser-precise floor plans faster than any other service.",
  img: "https://picsum.photos/200/350"
},
{
  id: 6,
  title: 'Video',
  options: ["Drone Cinematography",
    "Interiors",
    "Exteriors / Architectural"],
  description: "Video content has higher engagement and will help your property stand out online.",
  img: "https://picsum.photos/200/350"
},
]
</script>

<template>
  <div class="py-[108px]">
    <h1 class="text-[56px] text-[#1B264F] w-[730px] m-auto text-center mb-[80px]">
      We make creative media that <i class="text-[#506BCA]">adds value</i>
    </h1>
    <section class="mb-[80px]">
      <CardList :items="items" />
    </section>
    <div class="w-full flex justify-center">
      <button class="w-[199px] h-[60px] bg-[#1B264F] text-white rounded-lg">Get STARTED</button>
    </div>
  </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@600&family=Poppins:wght@700&display=swap');

* {
  font-family: 'Nunito', sans-serif;
  color: #353844;
  font-weight: 600;
}

ul,
li {
  font-weight: 700;
}

/* set the Poppins font for h tags */
h1,
h2,
h3,
h4,
h5,
h6,
i {
  font-family: 'Poppins', sans-serif;
}
</style>
