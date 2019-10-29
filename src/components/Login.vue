<template>

    <div>

        <input @input="onInput"/>

    </div>

</template>

<script>

    export default {
        name: 'Login',
        methods: {
            onInput: function (event) {
                this.$emit('termChange', event.target.value);
            }
        }
    };

</script>

<style></style>
