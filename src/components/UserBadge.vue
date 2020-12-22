<template>
    <div class="mainBadgeContainer">
        <h1>@{{user.userName}}</h1>
        <p>{{user.firstName}} {{user.lastName}}</p>
        <p><strong>Followers</strong> {{followers}}</p>
        <button @click="logMessage" class="btn btn-success">Follow</button>
    </div>
</template>

<script>
export default {
    name:'UserBadge',

    data(){
        return{
            followers:0,
            user:{
                userName: 'vicm',
                firstName: 'Victor',
                lastName: 'Meza',
            }
        }
    },
    watch: {

    },

    methods: {
        logMessage(){
            console.log("The button has been clicked.");
            this.followers++;
        }
    },

    components:{
        
    },

    computed:{

    },

    mounted(){

    }
}
</script>

<style scoped>
    .mainBadgeContainer{
        border-radius: 20px;
        width: 20vw;
        height: 25vh;
        background-color: whitesmoke;
        font-size: 1rem;
        display: flex;
        flex-direction: column;
        justify-content: center;
        color: black;
    }

    h1{
        font-size: 1.5rem;
        padding: 5px;
        text-align: center;
    }

    p{
        margin: auto;
    }

    button{
        margin: auto;
    }
</style>