<template>
<div class="home">
    <RegisterFrom />
</div>
</template>

<script lang="ts">
import {
    defineComponent
} from "vue";
import RegisterFrom from "@/modules/register/RegisterFrom.vue";

export default defineComponent({
    name: "Home",
    components: {
        RegisterFrom,
    },
});
</script>
