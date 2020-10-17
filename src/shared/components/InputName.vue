<template>
<div>
    <label for="nameInput">Name</label>
    <input id="nameInput" type="text" @input="handleInput" />
</div>
</template>

<script lang="ts">
import {
    defineComponent
} from "vue";

export default defineComponent({
    name: "InputName",
    props: {
        email: {
            type: String,
            default: "",
        },
    },
    setup(props, ctx) {
        const handleInput = (event: any) => {
            ctx.emit("update:name", event.target.value);
        };
        return {
            handleInput,
        };
    },
});
</script>
