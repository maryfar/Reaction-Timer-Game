<template>
    <p>Reaction Time: {{ score }} ms</p>
    <p class="rank">{{ rank }}</p>

</template>

<script>
export default {
    props:['score'],
    data(){
        return {
            rank:null,
        }
    },
    mounted(){
        if (this.score<400){
            this.rank = "You are an expert"
        }
        else if (this.score<800){
            this.rank = "You are an intermediate"
        }
        else{
            this.rank = "You are a biginner "
        }
    }
}


</script>

<style>
.rank {
    font-size: 1.4em;
    color:#419e87;
    font-weight: 500;
}

</style>