<template>
    <div>
        <div class="small-font">Contract Length (Months)</div>
        <v-row>
            <v-col cols="12">
                <span class="starting-value">1 month</span>
                <span class="ending-value">12 months</span>
            </v-col>
            <v-col cols="12" class="mt-n9">
                <v-slider
                  hint="Im a hint"
                  max="50"
                  min="0"
                  value="0"
                ></v-slider>
            </v-col>
        </v-row>
    </div>
</template>
<script>
export default {
    
}
</script>