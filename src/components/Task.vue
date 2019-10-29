<template>


    <div>

        <p>{{subTask.name}}</p>
        <span v-html="subTask.description"></span>

    </div>


</template>

<script>

    export default {
        name: 'Task',
        props: ['subTask']
    };

</script>
