<script>
import axios from 'axios';
export default {
    name:"ProjectsList",
    data() {
        return {
            projects:[],
        }
    },
    created(){
        axios.get('http://127.0.0.1:8000/api/projects')
        .then((response)=>{
            this.projects= response.data;
        })
    }
}
</script>

<template>
    <section>
        <h1>Projects' List</h1>
    </section>
</template>

<style scoped></style>