<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar class="bg-white text-black shadow-2 rounded-borders">
        <!-- <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        /> -->

        <q-toolbar-title class="text-blue"> ncoding </q-toolbar-title>
        <q-btn label="login" class="bg-red" />
      </q-toolbar>
    </q-header>

    <!-- <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Essential Links </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer> -->

    <q-page-container>
      <router-view />
    </q-page-container>
    <div>
      <LoginComponent></LoginComponent>
    </div>
  </q-layout>
</template>

<script lang="ts">
// import { defineComponent, ref } from 'vue';
import { defineComponent } from 'vue';
// import EssentialLink from 'components/EssentialLink.vue';
import LoginComponent from 'components/LoginComponent.vue';

const linksList = [
  {
    title: 'Docs',
    caption: 'quasar.dev',
    icon: 'school',
    link: 'https://quasar.dev',
  },
];

export default defineComponent({
  name: 'MainLayout',

  components: {
    // EssentialLink,
    LoginComponent,
  },

  setup() {
    // const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      isLogin: true,
    };
  },
});
</script>
