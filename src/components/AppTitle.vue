<template>
    <h1 class="mr">
       <span class="word">Mirror</span>
       <span class="word">Image</span>
    </h1>
    <div>
        <img src="/public/marc-olivier-jodoin--TQUERQGUZ8-unsplash.jpeg" alt="">
    </div>
</template>

<script>
import anime from 'animejs';
    export default {
        data(){
            return{
               name: 'AppTitle',
            }
            
        },
        methods:{
        animateTitle(){
                const timeline = anime.timeline({loop: true})
                .add({
                    targets: '.mr .word',
                    scale: [14,1],
                    opacity: [0,1],
                    easing: "easeOutCirc",
                    duration: 800,
                    delay: (el, i) => 800 * i
                })
                .add({
                    targets: '.mr',
                    opacity: 0,
                    duration: 1000,
                    easing: "easeOutExpo",
                    delay: 1000
                });

                timeline.play()
                
            }
        },
        mounted() {
            this.animateTitle();
        },    
    };
</script>

<style lang="scss" scoped>
    .mr {
        font-weight: 800;
        font-size: 3.8em;
        text-transform: uppercase;
        letter-spacing: 0.5em;
        text-align: center;
        margin-top: 100px;
    }
    .mr .word {
        display: inline-block;
        line-height: 1em;
    }
    img{
        width: 500px;
        display: block;
        margin-left: auto;
        margin-right: auto;
        margin-top: 20px;
    }
</style>