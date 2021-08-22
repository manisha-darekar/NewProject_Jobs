<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    <router-link :to="{name:'Jobs'}">Jobs</router-link>

  </div>
  <button @click="redirect">Redirect</button>
  <button @click="back">Go Back</button>
  <button @click="forward">Go Forward</button>
  <router-view/>
</template>
<script>
export default {
  methods:
  {
    redirect(){
      this.$router.push({name:'Home'})

    },
    forward(){
      this.$router.go(1)
    },
    back(){
      this.$router.go(-1)


    }

  }
  
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
    color: #2c3e50;
    padding: 17px;
    text-decoration: none;
    background: rgb(3, 240, 224);
    border-radius: 7px;
    margin: 5px;
}

#nav a.router-link-exact-active {
  color: black;

}
button{
  
  border: none;
  border-radius: 8px;
  padding: 10px;
  margin: 10px;
  text-align: center;
  cursor: pointer;
}
</style>
