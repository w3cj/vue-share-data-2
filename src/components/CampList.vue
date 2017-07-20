<template lang="html">
  <section>
    <div class="panel panel-default" v-for="campsite in campsites">
      <div class="panel-heading">{{campsite.name}}</div>
      <div class="panel-body">
        {{campsite.description}}
        <small>{{campsite.location}}</small>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'CampList',
  props: ['campsites']
};
</script>

<style lang="css">
</style>
