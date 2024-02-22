<template lang="">
    <div>
       <h1>Main</h1> 
    </div>
</template>
<script>
import axios from 'axios';
export default {
    name: 'AppMain',
    data() {

    },
    methods: {
        getProjects() {
            axios.get('http://127.0.0.1:8000/api/projects', {
                params: {
                }
            })
                .then(function (response) {
                    console.log(response);
                })
                .catch(function (error) {
                    console.log(error);
                });
        },
    },
        created() {
            this.getProjects();
        }
    }
</script>
<style lang="">
    
</style>