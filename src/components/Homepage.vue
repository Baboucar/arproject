<template>
  <div>
    <Navigation/>
    <div class="marquee">
      <p class="marquee__paragraph">
      Le SERVICE-SMS simplifié commence aujourd'hui avec un essai gratuit de 14 jours.
Envoyer des SMS est le moyen le plus simple d’envoyer instantanément 10 ou 100 SMS en masse partout au Sénégal.
      </p>
    </div>

    <div class="slider">
      <img class="slider__image" src="/../images/background.jpg" alt="alt">
    </div>

    <section class="history container">
      <h2 class="history__title">Notre histoire :</h2>
      <p>
          Octopush est la version évoluée d’une précédente société spécialisée dans l’envoi de SMS créée en 2006 par le même fondateur. 
      </p>

      <p>
          Pushy-la-Pieuvre, mascotte reconnue et reconnaissable entre tous, est née de l’imagination du fondateur. Inspiré par son cher littoral Marseillais, près duquel il vit, il a invité par jeu de mots l’animal malicieux au cœur du langage marketing (la pieuvre se disant Octopus en anglais). 
      </p>
      <p>
          Chaque jour, l’équipe Octopush se dédie au développement de sa plateforme et à l’amélioration de ses services, avec pour chef de file l’emblématique Pushy-la-Pieuvre qui montre la voie à suivre d’un mouvement de tentacule.
      </p>
      <h2 class="history__title">Octopush, la mission :</h2>

      <p>
          Octopush propose des solutions d’envoi de SMS, simples d’utilisation, ergonomiques et à la pointe de la technologie adaptées à tous types de public. 
      </p>

      <p>
          L’équipe Octopush a développé un système permettant à ce jour un déploiement international grâce a une solution développée « in-house » en mode hébergé (SaaS, service as a software + API). 
      </p>
      <p>
          Octopush peut répondre aux problématiques d’envoi de SMS de chacun, de la PME aux grands groupes, des directions marketing aux agences de communication en passant par les sociétés informatiques. 
      </p>
    </section>
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

.history__title{
    color: #4b68b8;
}
@media (min-width: 64rem) {
  .marquee {
    background: #4b68b8;
    width: 100%;
    display: inline-block;
    color: #ffffff;
    

    &__paragraph {
      animation: marquee 50s linear infinite;
      text-align: right;

    }
  }

.container{
    width: 70%;
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