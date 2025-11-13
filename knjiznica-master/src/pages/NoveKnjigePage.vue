<template>
   <q-toolbar class="bg-red-9 text-white">
      <q-toolbar-title>
        Nove Knjige
      </q-toolbar-title>
    </q-toolbar>
  <q-page padding>
    <div class="q-pa-md row items-start q-gutter-md">
      <q-card class="my-card">
        <img src="https://www.vbz.hr/wp-content/uploads/2019/01/inferno_filmska.jpg">

        <q-card-section>
          <div class="text-h6">Inferno</div>
          <div class="text-subtitle2">by Dan Brown</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ inferno }}
        </q-card-section>
      </q-card>

        <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">

        <q-card-section>
          <div class="text-h6">Our Changing Planet</div>
          <div class="text-subtitle2">by John Doe</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ lorem }}
        </q-card-section>
      </q-card>

      <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">

        <q-card-section>
          <div class="text-h6">Our Changing Planet</div>
          <div class="text-subtitle2">by John Doe</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ 123}}
        </q-card-section>
      </q-card>

        <q-card class="my-card">
        <img src="https://cdn.quasar.dev/img/mountains.jpg">

        <q-card-section>
          <div class="text-h6">Our Changing Planet</div>
          <div class="text-subtitle2">by John Doe</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          {{ lorem }}
        </q-card-section>
      </q-card>
    
    </div>

  </q-page>
</template>

<script>
export default {
  setup () {
    return {
      inferno:'Brown i u ovom romanu ostaje vjeran intrigantnim i kontroverznim temama: Da Vincijev kod pokušao je osvijetliti prošlost drugačiju od one koju smo mislili da poznajemo, a Inferno nam pokazuje koliko je krhka svaka vizija naše budućnosti.',
      lorem: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.'
    }
  }
}
</script>
<style lang="sass" scoped>
.my-card
  width: 100%
  max-width: 250px
</style>