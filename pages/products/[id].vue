<template>
  <p>Product details for {{id}}</p>
  <button @click="Go">Go</button>
</template>

<script>
export default {
  data() {
    return {
      router: useRouter(),
      id : useRoute().params.id
    }
  },
  methods: {
    Go(){
      this.router.push("/")
    }
  }
}
</script>

<style>

</style>