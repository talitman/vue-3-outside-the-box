<template>
<div>
    <h1>Register</h1>
    <hr />
    <form>
        <InputEmail v-model:email="email" />
        <InputName v-model:name="fullName" />
    </form>
    email {{ email }} name {{ fullName }}
</div>
</template>

<script lang="ts">
import {
    defineComponent,
    defineAsyncComponent,
    ref
} from "vue";
import InputName from "@/shared/components/InputName.vue";

const InputEmail = defineAsyncComponent(
    () => import("@/shared/components/InputEmail.vue")
);

export default defineComponent({
    components: {
        InputEmail,
        InputName,
    },

    setup() {
        const email = ref("");
        const fullName = ref("");
        return {
            email,
            fullName,
        };
    },
});
</script>
