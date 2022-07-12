<template>
  <q-layout>
    <div>
      <h3>login</h3>
    </div>
  </q-layout>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'LoginComponent',
  data() {
    return {
      login: {
        username: 'default@demo.com',
        password: '123456',
      },
    };
  },
});
</script>

<style lang="sass">
.my-card
  width: 100%
  max-width: 250px
</style>
