
<!-- nested route page, only the part in the nuxt-child would change
the content loaded in the nuxt-child would be from users/index.vue -->

<template>
    <div class="">
    <!-- <h1>this is a vue users page</h1> -->
    <input type="text" v-model="userId">
    <button @click="onLoadUser">Load User</button>
    <nuxt-child /> <!-- marks the postion where different sections of neted routes should be loaded -->
</div>
</template>

<script>
export default {
    data() {
        return {
            userId:''
        }
    },
    methods: {
        onLoadUser() {
            this.$router.push('/users/' + this.userId);
        }
    },
    layout:'users' // only understood by nuxtjs. points to the file in layout/users.vue
}
</script>