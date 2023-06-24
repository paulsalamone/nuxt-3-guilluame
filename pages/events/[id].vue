<template>
    <div class="bg-yellow-600 h-screen">
        <h1 class="font-sans text-3xl">
            Event id: {{ $route.params.id }}
           <br/>
           Hash: {{ $route.hash }}
           <br/>
           Query: {{ $route.query}}


        </h1>
    </div>
    </template>