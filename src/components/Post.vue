<template>
    <div class="post-container">
        <div class="username-container">
            @{{username}}
        </div>
        <div class="content-container">
            {{Post.content}}
        </div>
    </div>
</template>

<script>
export default {
    name:'Post',
    props: {
        username: {
            type: String,
            required: true
        },
        Post: {
            type: Object,
            required: true
        }
    }
}
</script>






<style scoped>
    .post-container{
        border-radius: 0px;
        background: linear-gradient(315deg, #c9cacb, #eff0f1);
        box-shadow:  -9px -9px 19px #bebebf, 
             9px 9px 19px #ffffff;
        margin-top: 20px;
        margin-bottom: 20px;
        margin-right: 0px;
        margin-left: 20px;
        padding: 5px;
        cursor: pointer;
        transition: all .25s ease;
    }

    .post-container:hover{
        transform: scale(1.1 , 1.1);
    }
</style>