<template>
  <h1>the job id is {{id}}</h1>
</template>

<script>
export default {
    data(){
        return{
            id:this.$route.params.id
        }
    }

}
</script>

<style>

</style>