<template>
    <div id="posts-container">
        <Post v-for="post in user.posts" :key="post.id" :username="user.userName" :Post="post" />
    </div>    
</template>

<script>
import Post from './Post.vue';


export default {
    name: 'Feed',
    data(){
        return{
            user:{
                userName: 'vicm',
                firstName: 'Victor',
                lastName: 'Meza',
                posts: [
                {id: 1, content: 'This is my first post'},
                {id: 2, content: 'This is the second post'},
                {id: 3, content: 'this is the third post'},
                {id: 4, content: "this will be the longest post I ever make, this is goinf to last all of this block lolol I just wanted to see what length I could get away with ofcourse"},
                {id: 5, content: "this will be the longest post I ever make, this is goinf"+ 
                "to last all of this block lolol I just wanted to see what length I could get"+
                "away with ofcourse this will be the longest post I ever make, this is goinf to"+
                "last all of this block lolol I just wanted to see what length I could get away with "+
                "ofcourse this will be the longest post I ever make, this is goinf "+
                "to last all of this block lolol I just wanted to see what length I could get"+
                "away with ofcourse this will be the longest post I ever make, this is goinf to"+
                "last all of this block lolol I just wanted to see what length I could get away with ofcourse"}
                ]
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
        Post
        
    },

    computed:{

    },

    mounted(){

    }
}
</script>


<style scoped>
    .posts-container{
        margin-left: 5vw;
        position: absolute;
        left: 20%;
        max-width: 80vw;
    }
</style>