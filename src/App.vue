<template>
  <div id="app">
    <header class="page-header container">
      <h1>{{message}}</h1>
    </header>
    <main class="container">
      <Campsites></Campsites>
    </main>
  </div>
</template>

<script>
import Campsites from './components/Campsites';

export default {
  name: 'app',
  components: {
    Campsites
  },
  data() {
    return {
      message: 'Share Data',
    };
  }
};
</script>

<style>
</style>
