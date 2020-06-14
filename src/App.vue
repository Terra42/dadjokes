<template>
  <div class="container">
    <joke
      v-for="(joke, index) in jokes"
      :user="joke.user"
      :text="joke.text"
      :likes="joke.likes"
      :dislikes="joke.dislikes"
      :key="joke.user"
    />
  </div>
</template>

<script>
import Joke from "./components/Joke.vue";

export default {
  name: "App",

  components: {
    joke: Joke
  },

  data() {
    return {
      jokes: [
        {
          user: "user01",
          text: `The secret service isn't allowed to yell "Get down!" anymore when the president is about to be attacked. Now they have to yell "Donald, duck!"`,
          likes: 13,
          dislikes: 24
        },
        {
          user: "user02",
          text: `Why did the invisible man turn down the job offer? He couldn't see himself doing it.`,
          likes: 50,
          dislikes: 10
        },
        {
          user: "user03",
          text: `I bought some shoes from a drug dealer. I don't know what he laced them with, but I was tripping all day!`,
          likes: 30,
          dislikes: 2
        },
        {
          user: "user04",
          text: `Did you hear the news? FedEx and UPS are merging. They’re going to go by the name Fed-Up from now on.`,
          likes: 15,
          dislikes: 8
        },
        {
          user: "user05",
          text: `My daughter screeched, "Daaaaaad, you haven't listened to one word I've said, have you!?" What a strange way to start a conversation with me...`,
          likes: 90,
          dislikes: 44
        },
        {
          user: "user06",
          text: `My wife tried to unlatch our daughter's car seat with one hand and said, "How do one armed mothers do it?" Without missing a beat I replied, "Single handedly."`,
          likes: 38,
          dislikes: 1
        },
        {
          user: "user07",
          text: `When a dad drives past a graveyard: Did you know that's a popular cemetery? Yep, people are just dying to get in there!`,
          likes: 66,
          dislikes: 35
        },
        {
          user: "user08",
          text: `My friend keeps saying "cheer up man it could be worse, you could be stuck underground in a hole full of water." I know he means well.`,
          likes: 27,
          dislikes: 18
        },
        {
          user: "user09",
          text: `The fattest knight at King Arthur’s round table was Sir Cumference. He acquired his size from too much pi.`,
          likes: 42,
          dislikes: 9
        }
      ]
    };
  }
};
</script>

<style lang="css">
* {
  box-sizing: border-box;
}

html {
  font-family: sans-serif;
}

.container {
  max-width: 30rem;
  margin: 5rem auto;
}
</style>