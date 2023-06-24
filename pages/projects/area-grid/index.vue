<template>
    <div class="bg-gray-100 h-screen p-3">
        <h2 class="text-2xl mx-5">Random Area Grid</h2>
        <p class="mx-7 italic">Goal: a 9-cell grid-area grid that randomizes on each button press, plus colors.</p>
        <p>{{ output }}</p>
        <button class="py-3 px-10 mt-5 ml-7 text-white rounded-full bg-teal-900 hover:bg-teal-700" @click.prevent="handleGrid">{{gridState ? "Refresh Grid" : "Create Grid"}}</button>
        <div class="grid grid-areas" >
            <!-- v-if="gridState" -->
<div  v-for="(cell, index) in cells" :key="index" class="cell-base" >{{ cell.name }}</div>
        </div>
    </div>
</template>

<script setup>
import {ref} from "Vue"

const gridState = ref(false)

const output = ref([])
const handleGrid = () => {
    gridState.value = true;

    const initialRows = Math.floor(Math.random() * 6);
cells.value = []
for(let i = 0; i < initialRows; i++){
    cells.value.push([])

    const secondaryRows = Math.floor(Math.random() * 6);

    for(let j = 0; j < secondaryRows; j++){
    cells.value.push({name: "x"})


}

}


}


const cells = ref([
]
)

</script>
<style scoped>
.grid {
    height: 500px;
    width: 500px;
    border: 3px solid white;
    outline:  3px solid black;
    background-color: #aaa;
    margin: 2rem;
    display: grid;
    gap: 10px;
    padding: 10px;
   grid-template-rows: 1fr 1fr 1fr 1fr;
   grid-template-columns: 1fr 1fr 1fr 1fr;

}


.cell-base {
    border: 1px solid black;
    box-shadow: 0 0 5px rgba(0, 0, 0, 0.359);

}

</style>