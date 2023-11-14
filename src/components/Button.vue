<template>
    <button
        class="btn"
        v-on:click="onClick()"
        v-bind:style="{ background: color }"
    >
        {{ text }}
    </button>
</template>

<script>
export default {
    name: "Button",
    props: {
        text: {
            type: String,
            default: "Click",
        },
        color: {
            type: String,
            default: "#fff",
        },
    },
    methods: {
        onClick() {
            console.log("click");
        },
    },
};
</script>
<style scope></style>
