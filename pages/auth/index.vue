<template>
    <div class="form">
        <div class="input">
            <input type="text" v-model="email" placeholder="Seu melhor email...">
        </div>
        <div class="input">
            <input type="password" v-model="password" placeholder="Sua Senha...">
        </div>

        <button @click="onSubmit" class="entry">Entrar</button>

    </div>


</template>
<script>
definePageMeta({
    layout: "auth"
})

import axios from "axios"
export default {
    data() {
        return {
            email: "",
            password: ""
        }
    },
    methods: {
        onSubmit() {
            axios.post("http://localhost:3001/login",
                { email: this.email, password: this.password })
                .then(response => {
                    console.log(response.data.data)
                })
                .catch(error => {
                    console.error(error.response.data.errorPassword);
                })
            // await useFetch("http://localhost:3001/login", {
            //     method: "post",
            //     body: { email: this.email, password: this.password }
            // }).then(response => {

            // console.log(response.data)
            // })

        }
    }
}
</script>

<style scoped>

</style>