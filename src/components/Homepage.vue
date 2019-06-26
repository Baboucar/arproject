<template>
    <div>
    <Navigation/>
     <div class="marquee">
         <p class="marquee__paragraph">
            This is just a test
         </p>

     </div>
     <div class="slider">
         <img class="slider__image" src="/../images/slider.jpeg" alt="">
     </div>
    </div>
</template>

<script>
import Navigation from '../components/Navigation';
    export default {
        components:{
            Navigation
        }
        
    }
</script>

<style lang="scss" scoped>
 .marquee{
     background: #4b68b8;
     width: 100%;
     display: inline-block;
     color: #FFFFFF;
     font-size: 1.5rem;

     &__paragraph{
         animation: marquee 30s linear infinite;
         text-align: right;
     }

 }

 @keyframes  marquee{
     0%{transform: translate(0,0);}
     100% {transform: translate(-100%,0);}
 }
  .slider__image{
      width:100%;
      max-width: 100%;
      height: auto;
  }
</style>