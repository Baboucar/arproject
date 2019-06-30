<template>
  <div>
    <Navigation/>
    <div class="marquee">
      <p class="marquee__paragraph">
        Textuellement : Le SERVICE-SMS simplifié commence aujourd'hui avec un essai gratuit de 14 jours. <br>
        
        Envoyer des SMS est le moyen le plus simple d’envoyer instantanément 10 ou 100 SMS en masse partout au Sénégal. <br>
        Service-sms n'a jamais été aussi facile.
        Essayez-le gratuitement.
        Pas de carte de crédit nécessaire.
        Discuter avec nous en direct.
      </p>
    </div>
    <div class="slider">
      <img class="slider__image" src="/../images/background.jpg" alt="alt">
    </div>
  </div>
</template>

<script>
import Navigation from "../components/Navigation";
export default {
  components: {
    Navigation
  }
};
</script>

<style lang="scss" scoped>
.marquee {
  display: none;
}
@media (min-width: 64rem) {
  .marquee {
    background: #4b68b8;
    width: 100%;
    display: inline-block;
    color: #ffffff;
    font-size: 1.5rem;
    
    &__paragraph {
      animation: marquee 50s linear infinite;
      text-align: right;
      font-size: .9rem;
    
    }
  }

  @keyframes marquee {
    0% {
      transform: translate(0, 0);
    }
    100% {
      transform: translate(-100%, 0);
    }
  }
  .slider__image {
    width: 100%;
    max-width: 100%;
    height: auto;
  }
}
</style>