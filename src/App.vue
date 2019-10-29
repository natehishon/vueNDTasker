<template>

    <div id="app">

        <div class="slide-show-container">
            <coverflow id="coverflow" :coverList="coverList" :coverWidth="260" v-on:change="onTermChange"></coverflow>
        </div>


        <div class="task-container">
            <Task :subTask="subTaskList[currentIndex]"></Task>
        </div>

    </div>


</template>

<style>

    #coverflow {
        overflow-x: visible !important;

    }

    .slide-show-container {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: center;
    }

    .task-container {
        display: flex;
        flex-direction: row;
        flex-wrap: nowrap;
        justify-content: center;
    }


</style>

<script>

    import coverflow from 'vue-coverflow'
    import Task from "./components/Task";


    export default {
        name: 'App',
        components: {
            Task,
            coverflow
        },
        data() {
            return {

                subTaskList: [
                    {
                        name: 'Subtask one',
                        description: 'sub task one description'
                    },
                    {
                        name: 'Subtask two',
                        description: 'sub task two description'
                    },
                    {
                        name: 'Subtask three',
                        description: '<span style="color: red">YO</span>'
                    },
                    {
                        name: 'Subtask four',
                        description: 'sub task one description'
                    },
                ]
                ,

                currentIndex: 0,

                coverList: [
                    {
                        cover: './img/icons/font-awesome_4-7-0_address-card_256_10_2c3e50_none.png',
                        title: 'Fill out profile'
                    }, {
                        cover: './img/icons/feather_1-1-0_columns_256_10_2c3e50_none.png',
                        title: 'Set column data'
                    }, {
                        cover: './img/icons/mfg-labs-iconset_2014-07-29_math_256_10_2c3e50_none.png',
                        title: 'Process column one'
                    },
                    {
                        cover: './img/icons/font-awesome_4-7-0_check-circle_256_10_2ecc71_none.png',
                        title: 'Turn in!'
                    },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Webpack'
                    // }, {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Yarn'
                    // }, {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // }
                    // ,{
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // },
                    // {
                    //     cover: 'https://upload.wikimedia.org/wikipedia/en/a/a6/Pok%C3%A9mon_Pikachu_art.png',
                    //     title: 'Node'
                    // }

                ]
            }
        },
        methods: {
            onTermChange(index) {

                this.currentIndex = index;

            }
        }
    }

</script>
