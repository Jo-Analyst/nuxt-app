<template>
    <div>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="about">About</NuxtLink>

        <br>
        <hr>
        <button @click="moveToAbout">Take me to About Page</button>
       <p> Hello Index</p>
    </div>

</template>
<script>
export default {
    methods: {
        moveToAbout() {
            navigateTo("about")
        }
    }
}
</script>