<template>

<h1>jobs</h1>
<div v-for="job in jobs" :key="job.id" class="jobs">
    <router-link :to="{name:'JobDetails', params:{id:job.id}}">
        <h2>{{job.title}}</h2>
    </router-link>
    
</div>

  
</template>

<script>
export default {
    data()
    {
        return{
            jobs:[{title:'web developer', id:1,details:'IT'},
                  {title:'web Designer', id:2,details:'Software'},
                  {title:'Photoshop', id:3,details:'Executive'}
                
            
            
            
            ]
        }
    }

}
</script>

<style>
.jobs h2{

    background: rgb(194, 184, 184);
    max-width: 600px;
   
    
    margin: 10px auto;
    border-radius: 20px;
    text-align: center;
    padding: 20px;
    color: rgb(64, 57, 57);
}
.jobs h2:hover{
    background:rgb(17, 221, 167);
}
.jobs a{
    text-decoration: none;
}

</style>