<script>
    export default {
             name:'ProjectCard',
             props:{
                info:Object,
             },   
    }
</script>

<template>
    <div class="card" style="width: 18rem;">
        <img class="card-img-top" src="..." alt="Card image cap">
        <div class="card-body">
            <div>
                <h5 class="card-title">{{ info.title }}</h5>
            </div>
            <hr>
            <div class="mb-3">
                Customer related:
                <p class="mt-2 card-text fw-bold">{{ info.client }}</p>
            </div>
            <hr>
            <a href="#" class="btn btn-primary">Read More</a>
        </div>
    </div>
</template>


<style lang="scss" scoped>

</style>