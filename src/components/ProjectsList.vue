<script>
import axios from 'axios';
import ProjectCard from './ProjectCard.vue';
export default {
    name:"ProjectsList",
    components:{
        ProjectCard,
    },
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
        <div class="container">
            <h1 class="text-center">Projects' List</h1>
            <div class="row mt-5">
                <div class="col-3 mt-4" v-for="project in projects">
                    <ProjectCard :info="project" />
                </div>
            </div>
        </div>
    </section>
</template>

<style scoped></style>