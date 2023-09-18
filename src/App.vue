

<template>
  <select v-model="namedComponent">
    <option value="Home">Home</option>
    <option value="About">About</option>
  </select>
  <KeepAlive>
    <component :is="namedComponent"></component>
  </KeepAlive>
</template>

<!-- vue logic -->
<script>
import Home from './components/Home.vue';
import About from './components/About.vue';

export default {
  name:'App',
  components: {
    Home,
    About
  },
  data(){
    return {

    namedComponent: 'Home'
    }
  }
}
</script>
<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
