<template> 
<div>   <nav class="mt-5 border-2">
        <NuxtLink to="/" class="mx-3">Home</NuxtLink>
        <NuxtLink class="mx-3" @click.prevent="handleProjects">Projects</NuxtLink>
    </nav>
    <nav v-if="showProjects" class="bg-gray-200 ">
        <NuxtLink to="/projects/area-grid" class="mx-3">Area-Grid</NuxtLink>
    </nav>
        <!-- how do i do a subnav? -->

<!-- subnav here -->

    </div></template>

    <script>
export default {
    data(){
        return {
showProjects: false
        }
    },
    methods: {
        handleProjects(){
            this.showProjects = !this.showProjects
        }
    }
}
</script>