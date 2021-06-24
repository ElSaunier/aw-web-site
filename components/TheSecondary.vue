<template>
  <div class="TheSecondary">

    <header class="title">
        <span><img/><img/></span>
    </header>

    <div id="trailer-desc">
      <div class="container-desc container">
        <h2 id="title-desc">Project Overview</h2>

        <p class="desc">
          During our third year of computer science studies, we had to make a former solo game become a real time multiplayer game.
          Thus we have chosen the game Asteroid from the 80s. Thereby you're able to shoot others players while dodgeing asteroids.
          We hope you will enjoy our new version of this famous game !
        </p>
      </div>

      <div class="container-video container">
        <iframe class="video" src="https://www.youtube.com/embed/7KXGZAEWzn0"></iframe>
      </div>
    </div>


    <div id="tag-container">
      <div
        v-for="tag in tags"
        :key="tag.title"
        class="tag"
        >
        <styled-section
          :title="tag.title"
          :description="tag.desc"
        />
      </div>
    </div>

    <div id="social-list">
      <a class="social-link" id="reddit" href="https://www.reddit.com/user/Astrocket-devs"><img class="img" src= "../assets/images/logo-reddit.png"/> Astrocket-devs</a>
      <a class="social-link" id="twitter" href="https://twitter.com/AstrocketG"><img class="img" src= "../assets/images/logo-twitter.png"/> AstrocketG</a>
      <a class="social-link" id="discord" href="https://discord.gg/m3aBuZxjMp"><img class="img" src="../assets/images/logo-discord.png" />Astrocket</a>
    </div>

  </div>
</template>

<script>
import StyledSection from './StyledSection.vue'

export default {
  components: { StyledSection },
  name: "TheSecondary",
  data() {
    return {
      tags: [
        {
          title: "About us",
          desc: "We're a group of 11 IT student at the Strasbourg University in France. "
           + "We're in our Bachelor's degree. For our teaching unit we made a team together and we have to create a multiplayer version of an old game."
        },
        {
          title: "Asteroid the Game",
          desc: " The game Astroid is a spaceshooter. You're controlling a spaceship and you must survive into space. "
          + "But there is numerous asteroids that can kill you, in order to survive, you can destroy or dodge them. "
          + "Moreover, you're earning more points the longer you live. So the goal is to survive the longest time "
        },
        {
          title: "Astrocket multi",
          desc: "In order to add a multiplayer feature to the game, we had to choose what would it be. So, by playing AstRocket "
          + "you will have to destroy asteroids and destroy others players ships to win points. The player with the most amount of points win the game."
        }
      ]
    }
  }
}
</script>

<style>
.container{
  @apply flex flex-col;
}

.video{
  @apply p-3;
}

.container-desc{
  @apply text-center divide-y divide-blue-500 mr-4 leading-loose;
}

#social-list{
  @apply flex items-center shadow-md bg-gray-100 m-auto mb-4 mt-10 box-content justify-center divide-x divide-gray-300 pt-2 pb-2 w-1/3;
}

/*Width to change*/
.img{
  @apply w-10 m-1;
}

.social-link{
  @apply flex items-center pr-4 pl-4;
}

.desc{
  @apply p-3;
}

#title-desc{
  @apply font-sans font-bold font-mono capitalize p-2;
}

#trailer-desc{
  @apply flex p-4 m-4 bg-gray-100 divide-x divide-gray-300 shadow-md;
}

#tag-container{
  @apply flex p-4;
}

.tag{
  @apply justify-center text-center mx-auto box-border h-1/4 w-1/4 p-4 border-2 border-blue-200 rounded-lg shadow-md bg-gray-100;
}

</style>
