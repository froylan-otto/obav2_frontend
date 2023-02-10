<template>
  <q-layout view="lhh LpR lfr">
    <q-header class="bg-primary text-white" height-hint="98">
      <q-toolbar>
        <q-toolbar-title align="center">
          <q-avatar>
            <img src="https://cdn.quasar.dev/logo-v2/svg/logo-mono-white.svg" />
          </q-avatar>
          OBA
        </q-toolbar-title>
      </q-toolbar>

      <!-- <q-tabs align="center">
        <q-route-tab to="/page1" label="Page One" />
        <q-route-tab to="/page2" label="Page Two" />
        <q-route-tab to="/page3" label="Page Three" />
      </q-tabs> -->

      <div class="q-pa-sm bg-secondary" align="center" unelevated>
        <q-btn-group push unelevated>
          <q-btn
            color="primary "
            text-color="white"
            push
            icon="home"
            class="text-white"
          />
          <q-btn color="primary" text-color="white" push label="Dashboard" />
          <q-btn color="primary" text-color="white" push label="User account" />
          <q-btn color="primary" text-color="white" push label="Files" />
          <q-btn color="primary" text-color="white" push label="FAQ Site" />
          <q-btn color="primary" text-color="white" push label="Settings" />
        </q-btn-group>
      </div>
    </q-header>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";

export default {
  setup() {
    const rightDrawerOpen = ref(false);

    return {
      rightDrawerOpen,
      toggleRightDrawer() {
        rightDrawerOpen.value = !rightDrawerOpen.value;
      },
    };
  },
};
</script>
