<template>
    <div class="todo-item" v-bind:class="{'is-complete': item.isComplete}" >
        <input type="checkbox" v-on:change="markComplate">
        <p>{{item.title}} </p>

    </div>
</template>

<script>
export default {
    name:"TodoItem",
    props : ["item"],
    methods: {
        markComplate(){
            console.log(this.item.isComplete);
            this.item.isComplete = !this.item.isComplate;
        }

    }
}
</script>


<style scoped>

    .todo-item{
        background-color: darkseagreen;
        padding: 5px;
        border-bottom: 1px #ccc solid;

    }
    .is-complete{
        color: red;
        text-decoration: line-through;
    }
</style>