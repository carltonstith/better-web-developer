<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex xs12>
        <v-img
          :src="require('../assets/growth.png')"
          class="my-3"
          contain
          height="200"
        ></v-img>
      </v-flex>

      <v-flex mb-4>
        <h1 class="font-weight-bold mb-3">
          Become a Better Web Developer
        </h1>
        <p class="subheading font-weight-regular">
           This is a list containing 10 ways a professional can be a better web engineer. This list, far from exhaustive and is ever evolving, should be used by all engineers from junior to senior.
          <a href="https://github.com/carltonstith/better-web-developer" target="_blank">Source Code</a>
        </p>
      </v-flex>

      <v-expansion-panels>
          <v-expansion-panel
            v-for="(tip,i) in tips"
            :key="i"
          >
            <v-expansion-panel-header>
              <span id="title">{{ tip.title }}</span>
            </v-expansion-panel-header>
            <v-expansion-panel-content class="text text-left">
              {{ tip.text }}
            </v-expansion-panel-content>
          </v-expansion-panel>
      </v-expansion-panels>

    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'BetterDev',

  data: () => ({
    tips: [
      {
        title: 'Read other people\'s code',
        text: 'Learn how to write good code from senior developers. This is important. Learn what bad code looks like also. Good code is easy to read and elegant. Bad code is hard to read and not elegant. Get the picture? I recommend reading the book Clean Code by Robert C. Martin.',
      },
      {
        title: 'Get someone to read your code.',
        text: 'Criticism is good for your health. Embrace it. Code reviews and critques will help your growth as a web professional. Once a senior has reviewed your code, then you can refactor your code if necessary.',
      },
      {
        title: 'Fix bugs before writing new code.',
        text: 'Writing new code is great but it will not mean anything if this code is leaning on shaky ground. Stay on top of bugs before things get out of hand. Keep the console open and Unit test frequently',
      },
      {
        title: 'Learn a new technology.',
        text: 'Read a new book, take a tutorial, attend a conference, listen to a podcast, etc.',
      },
      {
        title: 'Keep it simple.',
        text: 'Keep things as simple as possible when building your projects. Keep the features to the bare minimum at first. Far too many projects get abandoned because of this. Maintian a razor sharp focus and concentrate on delivering a MVP. You can always come back and build on top of what\'s already shipped. Remember: Just Ship It.',
      },
      {
        title: 'Write a blog post about your code.',
        text: 'You don\'t really have a firm grasp about the subject if you can\'t explain it to a five year old. This task will help you solidify your learning.',
      },
      {
        title: 'Contribute to open source.',
        text: 'This will help you get involved in the community and reading other people\'s code.',
      },
      {
        title: 'Fix it, don\'t hack it.',
        text: 'If what you built is broken, fix it the right way. Your future self will thank you.',
      },
      {
        title: 'Increase code coverage by 1%.',
        text: 'Write a little bit of code every day for your personal project.',
      },
      {
        title: 'Leave your desk every hour.',
        text: 'Getting up and walking away time to time is good for your physical and mental health. I would even suggest investing in a standing desk.',
      }
    ]
  }),
};
</script>
<style>
@import url('https://fonts.googleapis.com/css?family=Merriweather|Montserrat&display=swap');

h1 {
  font-family: 'Merriweather', serif;
  font-size: 3rem !important;
  font-weight: 400;
  line-height: 3.125rem;
  letter-spacing: normal !important;
}
p {
  font-family: 'Montserrat', sans-serif !important;
}
.v-application #title { 
  font-family: 'Merriweather', serif !important;
}
.text {
  font-family: 'Montserrat', sans-serif !important;
}
</style>
