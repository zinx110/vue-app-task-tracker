<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <i class="fas fa-times" />
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script lang="ts">
export default {
    name: "Task",
    props: {
        task: Object,
    },
};
</script>

<style scoped>
.task {
    background: #f0f0ff;
    margin: 30px 10px;
    padding: 10px 20px;
    border-radius: 2px;
}
i {
    color: red;
}
h3 {
    display: flex;
    justify-content: space-between;
}
.reminder {
    border-left: 5px solid green;
}
</style>
