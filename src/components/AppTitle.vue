<template>
    <h1>
       Mirror Image
    </h1>
    <div>
        <img src="/public/marc-olivier-jodoin--TQUERQGUZ8-unsplash.jpeg" alt="">
    </div>
</template>

<script>
    export default {
        data(){
            return{
               name: 'AppTitle',
            }
            
        },
        methods:{

        }
        
    };
</script>

<style lang="scss" scoped>
    h1{
        text-align: center;
        margin-top: 20px;
        font-size: 100px;
    }
    img{
        width: 500px;
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 20px;
    }
</style>