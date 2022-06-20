<template>
    <footer>
        <p>
            Copyright &copy; 2022 | Build with &hearts; by Bil Abror
        </p>
        <div v-show="aboutPage">
            <router-link to="/about" v-show="true">About</router-link>
        </div>
    </footer>
</template>

<script>

    export default {
        name: "Footer",
        computed: {
            aboutPage() {
                if (this.$route.path !== '/about') {
                    return true
                } else {
                    return false
                }
            }
        }
    }
    </script>

    <style>
        a {
            color: #333;
        }

        footer {
            margin-top: 30px;
            text-align: center;
        }
    </style>