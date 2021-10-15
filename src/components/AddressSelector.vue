<template>
    <v-card class="wrapper" elevation="2">
        <!-- <google-map :center="{lat: 1.38, lng: 103.8}" :zoom="12" style="width: 100%; height: 500px">
          <ground-overlay source="./overlay.png" :bounds="{
                north: 1.502,
                south: 1.185,
                east: 104.0262,
                west: 103.5998,
            }" :opacity="0.5">
          </ground-overlay>
        </google-map> -->
        
        <v-img
          :lazy-src="gmapIMG"
         :src="gmapIMG"
         class="img"
        >
        <div class="internal-wrapper">
        <h2>Select Address</h2>
         <v-text-field
         value="19 Dapitan street South Cotobato"
            class="text-field"
            filled
            background-color="white"
            rounded
            dense
            prepend-inner-icon="mdi-map-marker"
          ></v-text-field>
        </div>
        </v-img>
        <!-- <img :src="gmapIMG" height="100%"/> -->
    </v-card>
</template>
<script>
import gmapIMG from '../assets/img/gmap-img.png'
export default {
  data(){
    return {
      gmapIMG: gmapIMG,
      pinSVG: '<svg xmlns="http://www.w3.org/2000/svg" height="24px" viewBox="0 0 24 24" width="24px" fill="#000000"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5c-1.38 0-2.5-1.12-2.5-2.5s1.12-2.5 2.5-2.5 2.5 1.12 2.5 2.5-1.12 2.5-2.5 2.5z"/></svg>'
    
    }
  }
}
</script>
<style scoped>
.wrapper{
  height:300px;
  border-radius: 1%;
  overflow: hidden;
  text-align: initial;
  
  align-items: center;
}
.text-field{
  max-width: 500px;
  /* border:solid black 1px; */
}
.img{
  align-items: center;
}
.internal-wrapper{
  margin: 30px;
}
</style>