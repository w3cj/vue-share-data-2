<template>
  <div>
    <CampForm
      :onAddCampsite="onAddCampsite">
    </CampForm>
    <br>
    <CampList
      :campsites="campsites">
    </CampList>
  </div>
</template>

<script>
import CampForm from './CampForm';
import CampList from './CampList';
import campsites from '../lib/Campsites';

export default {
  name: 'Campsites',
  components: {
    CampForm,
    CampList
  },
  data() {
    return {
      message: 'Share Data',
      campsites
    };
  },
  methods: {
    onAddCampsite(campsite) {
      this.campsites.push(campsite);
    }
  }
};
</script>

<style>
</style>
