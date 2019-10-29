<template>

    <ul>

        <Task v-for="(task, index) in tasks" v-bind:task="task" :key="index">

        </Task>

    </ul>

</template>


<script>

    import Task from './Task'

    export default {
        name: 'TaskList',
        props: ['tasks'],
        components: {
            Task
        }
    }

</script>

<style></style>
