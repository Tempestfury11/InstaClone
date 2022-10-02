<template>
  <q-layout view="lHh Lpr lFf">
    <q-header
      class="bg-white text-grey-10"
      bordered>

      <q-toolbar
      class="constrain">

        <q-btn
        to="/camera"
        class="large-screen-only q-mr-sm"
        dense
        flat
        round
        icon="eva-camera-outline"
        size="18px" />

        <q-separator
        class="large-screen-only"
        vertical
        spaced
         />

        <q-toolbar-title
        class="text-grand-hotel text-bold">
          InstaClone
        </q-toolbar-title>

        <q-btn
        to="/"
        class="large-screen-only"
        dense
        flat
        round
        icon="eva-home-outline"
        size="18px" />

      </q-toolbar>
    </q-header>

    <q-footer
    bordered
    class="bg-white small-screen-only">
          <q-tabs
          class="text-grey-10"
          active-color="primary"
          indicator-color="transparent">

            <q-route-tab
            to="/"
            icon="eva-home-outline"
             />

            <q-route-tab
            to="/camera"
            icon="eva-camera-outline"
            />

          </q-tabs>
      </q-footer>

    <q-page-container class="bg-grey-1">
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from 'vue'

const linksList = [

]

export default defineComponent({
  name: 'MainLayout',


  setup () {

    return {

    }
  }
})
</script>

<style lang="sass">
.q-toolbar
 @media (min-width: $breakpoint-sm-min)
  height:77px

.q-toolbar__title
 font-size: 30px
 @media (mix-width: $breakpoint-xs-max)
  text-align: center

.q-footer
 .q-tab_tab_icon
  font-size: 30px
</style>
