<template>
  <div class="q-pa-md row items-start q-gutter-md">

    <q-card class="my-card">
      <q-img src="src/assets/quasar.png">
        <div class="absolute-bottom">
          <div class="text-h6 title">QUASAR</div>
          <div class="text-subtitle2"> </div>
        </div>
      </q-img>
      <q-card-actions>
        <q-btn flat>Site</q-btn>
        <q-btn flat>Notes</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img src="src/assets/vue.png">
        <div class="absolute-bottom">
          <div class="text-h6 title">VUE</div>
          <div class="text-subtitle2"> </div>
        </div>
      </q-img>
      <q-card-actions>
        <q-btn flat>Site</q-btn>
        <q-btn flat>Notes</q-btn>
      </q-card-actions>
    </q-card>

    <q-card class="my-card">
      <q-img src="src/assets/cordova.png">
        <div class="absolute-bottom">
          <div class="text-h6 title">CORDOVA</div>
          <div class="text-subtitle2"> </div>
        </div>
      </q-img>
      <q-card-actions>
        <q-btn flat>Site</q-btn>
        <q-btn flat>Notes</q-btn>
      </q-card-actions>
    </q-card>

  </div>

</template>

<script>
  import { defineComponent } from 'vue'

  export default defineComponent({
    name: 'ContentPage',

  });

</script>

<style lang="scss" >
.my-card{
  width: 100%;
  height: 100%;
  max-width: 250px;
}

.title{
  position: relative;
}

</style>
