<template>
    <h1>hello from the id subroute: {{$route.params.id}}</h1>    
</template>

<script>
export default {
    // validation property
    // special method nuxtjs executes before rendering a route
    validate(data) {
        console.log(data);
        // validate should return true in order to get the page rendered
        return /^\d+$/.test(data.params.id); // check if the paramter is number regex
    },
    layout:'users'
}
</script>