<template>
    <h1>{{name}}</h1>
    <h2>{{age}}</h2>
    <h3>{{birthplace}}</h3>
    <h4>{{currentLocation}}</h4>
    <hr/>
    <NameComp :name="name" />
    <AgeComp :age="age" />
    <BirthplaceComp :birthplace="birthplace"/>
    <CurrentLocationComp :currentLocation="currentLocation" />
  
</template>

<script setup>
    import {ref} from 'vue';

defineProps({
    name: {
        type: String,
        required: true,
    },
    age: {
        type: Number,
    },
    birthplace:{
        type: String,
        default: "World",
    },
    currentLocation: {
        type: String,
    },
});

</script>

<style>

</style>