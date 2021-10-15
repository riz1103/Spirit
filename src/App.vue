<template>
  <v-app>
    <!-- <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>

      <v-btn
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
        text
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar> -->

    <v-main class="app-style">
      <v-row>
        <AddressSelector/>
      </v-row>
      <v-row>
        <v-col cols="4" class="margin-less-left">
          <FilterArea/>
        </v-col>
        <v-col cols="8" class="margin-less-right">
          <PlanCard/>
          <PlanCard/>
        </v-col>
      </v-row>
      <!-- <HelloWorld/> -->
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';
import AddressSelector from './components/AddressSelector.vue';
import FilterArea from './components/Filter.vue';
import PlanCard from './components/PlanCard.vue';

export default {
  name: 'App',

  components: {
    HelloWorld,
    FilterArea,
    AddressSelector,
    PlanCard
  },

  data: () => ({
    //
  }),
};
</script>
<style scoped>
.app-style{
  text-align: center;
  max-width:1000px;
  margin:50px;
}
.margin-less-left{
  padding-left:0px;
}
.margin-less-right{
  padding-right:0px;
}
</style>
