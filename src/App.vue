<template>
    <div class="container">
        <Header @toggle-add-task="toggleAddTask" title="Vue Task" :showAddTask="showAddTask" />
        <router-view :showAddTask="showAddTask"></router-view>
        <Footer />
    </div>
</template>

<script>

    import Header from "./components/Header"
    import Footer from "./components/Footer"

    export default {
        name: 'App',
        components: {
            Header,
            Footer
        },
        data() {
            return {
                showAddTask: false
            }
        },
        methods: {
            toggleAddTask() {
                this.showAddTask = !this.showAddTask
            }
        }
    }

    </script>


    <style>


@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;&display=swap');

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        body {
            font-family: "Poppins",'arial',Sans-Serif;
            background: #aaa;
        }

        .container {
            max-width: 500px;
            margin: 30px auto;
            overflow: auto;
            min-height: 300px;
            border: 1px solid grey;
            padding: 30px;
            border-radius: 5px;
            background: #ddd;
        }
        .container:hover {
            transition: .5s;
            transform: scale(1.02);
            border: 1px solid steelblue;
            box-shadow: 5px 5px 5px steelblue;

        }

        .btn {
            display: inline-block;
            background: #000;
            color: #fff;
            border: none;
            padding: 10px 20px;
            margin: 5px;
            border-radius: 5px;
            cursor: pointer;
            text-decoration: none;
            font-size: 15px;
            font-family: inherit;
        }

        .btn:focus {
            outline: none;
        }

        .btn:active {
            transform: scale(0.98);
        }

        .btn-block {
            display: block;
            width: 100%;
        }

    </style>