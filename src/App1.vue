<template>
    <div id="app">

        <ol>
            <todo-item v-for='item in groceryList' v-bind:todo="item" v-bind:key="item.id"></todo-item>
        </ol>

       <Event v-bind:name="name"></Event>      
    </div>
</template>

<script>
    import TodoItem from './components/TodoItem.vue'
    import Event from './components/Event.vue'



    export default {
        data() {
            return {

                groceryList: [{
                    id: 0,
                    text: '蔬菜123'
                }, {
                    id: 1,
                    text: '奶酪'
                }, {
                    id: 2,
                    text: '芒果'
                }],
                name:name
            }
        },
        components: {
            TodoItem,
            Event,
        }
    }



</script>