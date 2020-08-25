<template>
    <div id="computed">
        <h1>Computed</h1>
        <input type="text" v-model="findName">
        <ul>
            <li v-for="user in filterUsers" :key="user">{{user}}</li>
        </ul>
        
    </div>
</template>

<script>
export default {
    name:"Computed",
    data: () =>({
        findName:"",
        users:["Claude", "Junior", "Francois","Christian"]
    }),
    computed: {
        filterUsers(){
            return this.users.filter(user => user.match(this.findName))
        }

    }
    
};
</script>

<style>
    

    
</style>