<template lang="html">
  <form class="form">
    <div class="form-group">
      <label for="name">Name</label>
      <input v-model="campsite.name" type="text" class="form-control" id="name" placeholder="">
    </div>
    <div class="form-group">
      <label for="location">Location</label>
      <input v-model="campsite.location" type="text" class="form-control" id="location" placeholder="">
    </div>
    <div class="form-group">
      <label for="description">Description</label>
      <input v-model="campsite.description" type="text" class="form-control" id="description" placeholder="">
    </div>
    <button @click="addCampsite" type="button" class="btn btn-default">
      Add Campsite
    </button>
  </form>
</template>

<script>
export default {
  name: 'CampForm',
  props: ['onAddCampsite'],
  data() {
    return {
      campsite: {
        name: '',
        location: '',
        description: ''
      }
    };
  },
  methods: {
    addCampsite() {
      this.onAddCampsite({
        name: this.campsite.name,
        location: this.campsite.location,
        description: this.campsite.description
      });

      this.campsite.name = '';
      this.campsite.location = '';
      this.campsite.description = '';
    }
  }
};
</script>

<style lang="css">
</style>
