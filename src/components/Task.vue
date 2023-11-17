<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <i @click="onDelete(task.id)" class="fas fa-times" />
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent ({
    name: "Task",
    props: {
        task: Object,
    },
    setup(props,(emit)){
        const  onDelete=(id: number)=> {
            emit("delete-task", id);
        }
        return onDelete;
    }

});
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
    cursor: pointer;
}
h3 {
    display: flex;
    justify-content: space-between;
}
.reminder {
    border-left: 5px solid green;
}
</style>
