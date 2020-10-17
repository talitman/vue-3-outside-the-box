<template>
<div>
    <label for="emailInput">Email</label>
    <input id="emailInput" type="email" @input="handleInput" />
</div>
</template>

<script lang="ts">
import {
    defineComponent
} from "vue";

export default defineComponent({
    name: "InputEmail",
    props: {
        email: {
            type: String,
            default: "",
        },
    },
    setup(props, ctx) {
        const handleInput = (event: any) => {
            ctx.emit("update:email", event.target.value);
        };
        return {
            handleInput,
        };
    },
});
</script>
