<template>
  <q-page class="constrain-more q-pa-md">
    <div class="camera-frame q-pa-md">
      <img
      class="full-width"
      src="https://i.postimg.cc/65sh2pHg/avataaars.png">
    </div>
    <div class="text-center q-pa-md">
      <q-btn
      size="lg"
      color="grey-10"
      icon="eva-camera"
      rounded
      />
      <div class="row justify-center q-ma-md">
        <q-input
        dense
        v-model="post.caption"
        class="col col-sm-6"
        label="Caption"
        />
      </div>
      <div class="row justify-center q-ma-md">
        <q-input
        dense
        v-model="post.location"
        class="col col-sm-6"
        label="Location"
        >
        <template v-slot:append>
          <q-btn
          round
          dense
          flat
          icon="eva-navigation-2-outline"
          />
        </template>
      </q-input>
      </div>
      <div class="row justify-center q-mt-lg">
        <q-btn
        unelevated
        rounded
        color="primary"
        label="Post Image" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from 'vue'
import { uid } from 'quasar'

export default defineComponent({
  name: 'PageCamera',
  data(){
    return{
      post:{
        id: uid(),
        caption: '',
        location: '',
        photo: null,
        date: Date.now()
      }
    }
  }
})
</script>

<style lang="sass">
.camera-frame
  border: 2px solid $grey-10
  border-radius: 10px
</style>
