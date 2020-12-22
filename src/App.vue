<template>
  <div class="badge">
    <UserBadge />
  </div>
  <div class="feed">
    <Feed />
  </div>  
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue'
//import CustomComponent from './components/Custom.vue'
import UserBadge from './components/UserBadge.vue'
import Feed from './components/Feed.vue'

export default {
  name: 'App',
  data(){
    return{
      followers: 0,
      isLoading: false,
      user: {
        username: 'Victor-meza-07',
        firstName: 'Victor',
        lastName: 'Meza',
        email: 'victord.meza@gmail.com',
        isAdmin: true
      }
    }
  },

  //this watches a data point and runs a function when theres is a change.
  //ngOnChange???
  watch:{
    //pass what the data is now, and what the data has changed to.
    //name of the function must be that of the data you are watching??
    followers(newFollowerCount, oldFollowerCount){
      if(oldFollowerCount < newFollowerCount){
        console.log(this.user.username + ' has gained a follower');
      }
    }
  },

  computed:{
    fullName(){
      return `${this.user.firstName} ${this.user.lastName}`;
    }
  },

  methods: {
    followUser(){
      this.followers ++;
    }
  },

  components: {
    //CustomComponent
    UserBadge,
    Feed
  },

  //ngOnInit
  mounted(){
    for (let index = 0; index < 150; index++) {
      this.followUser();
    }
  },

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100vw;
  height: 100vh;
  display: flex;
}

.badge{
position: absolute;
top: 0;
left: 0;
}
.feed{
  margin-left: 20px;
  width:80vw;
  position: absolute;
  left: 20vw;
}
</style>
