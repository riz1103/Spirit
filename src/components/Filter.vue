<template>
    <v-card class="wrapper" elevation="2">
        <div class="inner-wrapper">
            <h3>What are you looking for?</h3>
            <div class="sliders mt-5">
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
                <div>Current Load Speed (Mbps)</div>
                <v-row>
                    <v-col cols="12">
                        <span class="starting-value">1 Mbps</span>
                        <span class="ending-value">1000 Mbps</span>
                    </v-col>
                    <v-col cols="12" class="mt-n9">
                        <v-slider
                          hint="Im a hint"
                          max="1000"
                          min="0"
                          value="500"
                        ></v-slider>
                    </v-col>
                </v-row>
                <div>Max Price</div>
                <v-row>
                    <v-col cols="12">
                        <span class="starting-value">$1</span>
                        <span class="ending-value">$1000</span>
                    </v-col>
                    <v-col cols="12" class="mt-n9">
                        <v-slider
                          hint="Im a hint"
                          max="1000"
                          min="0"
                          value="0"
                        ></v-slider>
                    </v-col>
                </v-row>

                <v-btn>Reset Filters</v-btn>
            </div>
        </div>
    </v-card>
</template>
<script>
export default {
    name:'filter'
}
</script>
<style scoped>
    .wrapper{
        text-align: initial;
    }
    .inner-wrapper{
        margin:30px;
        padding-top: 30px;
        padding-bottom: 30px;
    }
    v-btn{
        align-self: center;
    }
    .starting-value{
        float: left;
        font-size: 12px;
    }
    .ending-value{
        font-size: 12px;
        float: right;
    }
</style>