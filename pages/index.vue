<template>
    <div>
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