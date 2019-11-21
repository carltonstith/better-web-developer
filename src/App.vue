<template>
  <v-app id="landing-page">
    <v-content>
      <BetterDev/>
    </v-content>
  </v-app>
</template>

<script>
import BetterDev from './components/BetterDev';

export default {
  name: 'App',
  components: {
    BetterDev,
  },
  data: () => ({
    //
  }),
};
</script>
<style>
#landing-page {
  background-image: radial-gradient( circle farthest-corner at 10% 20%,  rgba(255,246,236,1) 39.5%, rgba(100,46,122,0.23) 100.2% );
}
</style>
