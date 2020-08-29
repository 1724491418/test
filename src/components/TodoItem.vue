<template>
    <li class="test">{{todo.text}}</li>
</template>
<script>
    export default {
        props:['todo'],
    }

</script>

<style scoped>
    .test {
        color:#42b983;
    }
</style>