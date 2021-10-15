<template>
    <v-card class="wrapper" elevation="2">
        <div class="inner-wrapper">
            <v-row>
                <v-col>
                    <h2>250/250 Mbps</h2>
                    <div class="small-text">Download / Upload</div>
                    <div class="small-text">Only $350 per month + OST on a 48 month plan</div>
                </v-col>
                <v-col>
                    <h4>Data Plan</h4>
                    <v-row>
                        <v-col>
                            <div v-for="(pl,index) in plan" :key="pl">
                                <li class="small-text" v-if="index<5">
                                    <span v-html="checkIcon"></span>
                                    <span>{{pl}}</span>
                                </li>
                            </div>
                        </v-col>
                        <v-col>
                            <div v-for="(pl,index) in plan" :key="pl">
                                <li class="small-text" v-if="index>=5">
                                    <span v-html="checkIcon"></span>
                                    <span>{{pl}}</span>
                                </li>
                            </div>
                        </v-col>
                    </v-row>
                </v-col>
                <v-col class="align-self-center">
                    <v-btn  outlined depressed class="mb-5 button">View Brochure</v-btn>
                    <v-btn dark class="button" depressed>Enquire</v-btn>
                </v-col>
            </v-row>
        </div>        
    </v-card>
</template>
<script>
export default {
    data(){
        return {
            checkIcon: '<svg xmlns="http://www.w3.org/2000/svg" height="12px" viewBox="0 0 24 24" width="24px" fill="#418df2"><path d="M0 0h24v24H0z" fill="none"/><path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-2 15l-5-5 1.41-1.41L10 14.17l7.59-7.59L19 8l-9 9z"/></svg>',
            plan:[
                'Plan 100',
                'Plan 200',
                'Plan 300',
                'Plan 400',
                'Plan 500',
                'Plan 600',
                'Plan 700',
                'Plan 800',
                'Plan 900',
                'Plan 950',
            ]
        }
    }

}
</script>
<style scoped>
.wrapper{
        text-align: initial;
        border-left: solid #418df2 5px;
    }
.inner-wrapper{
        margin:30px;
        padding-top: 30px;
        padding-bottom: 30px;
    }
.small-text{
        font-size: 12px;
    }
li {
    list-style-type: none;
}
button{
    width: -webkit-fill-available;
}
</style>