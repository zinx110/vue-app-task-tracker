<template>
    <div v-bind:key="task.id" v-for="task in tasks"><Task :task="task" /></div>
</template>

<script>
import Task from "./Task.vue";

export default {
    name: "Tasks",
    props: {
        tasks: String,
    },
    components: {
        Task,
    },
};
</script>
