<template>
    <v-container fluid style="min-height:100vh" class="pa-0">
        <v-row class="no-gutters" style="height:100%">
            <v-col  class="no-gutters questionArea" cols="12" md="6" lg="6" xl="6" style="background-color:#000;color:#fff">
                <div class="pa-2 mt-10 text-center appTitle">
                    <b>Hello! Welcome to The Prediction of Covid-19 Infection App </b>
                </div>
                
                <div class="qsDivider mt-5"></div>
                
                <div class="pa-3">
                    <v-stepper
                            v-model="e6"
                            vertical
                            style="Background-color:#000"
                            dark
                        >
                        <!-- step 1 -->
                            <v-stepper-step
                                :complete="e6 > 1"
                                step="1"
                                >
                                Select your gender
                            </v-stepper-step>

                            <v-stepper-content step="1">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="gender"
                                    color="cyan"
                                    borderless
                                    mandatory
                                >
                                    <v-btn value="female">
                                        <span class="hidden-sm-and-down">Female</span>
                                    </v-btn>

                                    <v-btn value="male">
                                        <span class="hidden-sm-and-down">Male</span>
                                    </v-btn>

                                    <v-btn value="nb">
                                        <span class="hidden-sm-and-down">Non-Binary</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>
                            <v-btn
                                color="primary"
                                @click="e6 = 2"
                            >
                                Continue
                            </v-btn>
                            </v-stepper-content>

                            
                        <!-- step 2 -->

                            <v-stepper-step
                            :complete="e6 > 2"
                            step="2"
                            >
                            Select your age range
                            </v-stepper-step>

                            <v-stepper-content step="2">
                            
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="age"
                                    color="cyan"
                                    borderless
                                    mandatory
                                >
                                    <v-btn value="0-10">
                                        <span class="hidden-sm-and-down">0-10</span>
                                    </v-btn>

                                    <v-btn value="10-20">
                                        <span class="hidden-sm-and-down">10-20</span>
                                    </v-btn>

                                    <v-btn value="20-30">
                                        <span class="hidden-sm-and-down">20-30</span>
                                    </v-btn>

                                    <v-btn value="30-40">
                                        <span class="hidden-sm-and-down">30-40</span>
                                    </v-btn>

                                    <v-btn value="40-50">
                                        <span class="hidden-sm-and-down">40-50</span>
                                    </v-btn>

                                    <v-btn value="50-60">
                                        <span class="hidden-sm-and-down">50-60</span>
                                    </v-btn>

                                    <v-btn value=">60">
                                        <span class="hidden-sm-and-down">>60</span>
                                    </v-btn>


                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 3"
                            >
                                Continue
                            </v-btn>
                            <v-btn text  @click="e6 = 1">
                                Back
                            </v-btn>
                            </v-stepper-content>
                            
                            
                            <!-- step 3 -->

                            <v-stepper-step
                            :complete="e6 > 3"
                            step="3"
                            >
                            Select your level of smoking
                            </v-stepper-step>

                            <v-stepper-content step="3">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="smoking"
                                    color="cyan"
                                    mandatory
                                    borderless
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="no">
                                        <span class="hidden-sm-and-down">no smoking</span>
                                    </v-btn>

                                    <v-btn value="very low">
                                        <span class="hidden-sm-and-down">very low (1-2 a week)</span>
                                    </v-btn>

                                    <v-btn value="low">
                                        <span class="hidden-sm-and-down">low (4-5 a week)</span>
                                    </v-btn>

                                    <v-btn value="median">
                                        <span class="hidden-sm-and-down">median (every day)</span>
                                    </v-btn>

                                    <v-btn value="high">
                                        <span class="hidden-sm-and-down">high (3-5 every day)</span>
                                    </v-btn>

                                    <v-btn value="very high">
                                        <span class="hidden-sm-and-down">very high (>=1 pack everyday)</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 4"
                            >
                                Continue
                            </v-btn>
                            <v-btn text
                                @click="e6 = 2">
                                Cancel
                            </v-btn>
                            </v-stepper-content>


                            
                            <!-- step 4 -->
                            <v-stepper-step
                            :complete="e6 > 4"
                            step="4"
                            >
                            Do you experience any chest pain in the last 30 days?
                            </v-stepper-step>

                            <v-stepper-content step="4">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="chest"
                                    color="cyan"
                                    borderless
                                    mandatory
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="no">
                                        <span class="hidden-sm-and-down">no</span>
                                    </v-btn>

                                    <v-btn value="rarely">
                                        <span class="hidden-sm-and-down">rarely</span>
                                    </v-btn>

                                    <v-btn value="almost every day">
                                        <span class="hidden-sm-and-down">almost every day</span>
                                    </v-btn>

                                    <v-btn value="almost every day and very sore">
                                        <span class="hidden-sm-and-down">almost every day and very sore</span>
                                    </v-btn>
                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 5"
                            >
                                Continue
                            </v-btn>
                            <v-btn text 
                                @click="e6 = 3">
                                Cancel
                            </v-btn>
                            </v-stepper-content>

                            
                            <!-- step 5 -->
                            <v-stepper-step
                            :complete="e6 > 5"
                            step="5"
                            >
                           How many people you've meet in the last 30 days?
                            </v-stepper-step>

                            <v-stepper-content step="5">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="people"
                                    color="cyan"
                                    borderless
                                    mandatory
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="full isolation">
                                        <span class="hidden-sm-and-down">full isolation</span>
                                    </v-btn>

                                    <v-btn value="only core family">
                                        <span class="hidden-sm-and-down">only core family</span>
                                    </v-btn>

                                    <v-btn value="10-20 people">
                                        <span class="hidden-sm-and-down">10-20 people</span>
                                    </v-btn>

                                    <v-btn value="20-30 people">
                                        <span class="hidden-sm-and-down">20-30 people</span>
                                    </v-btn>

                                    <v-btn value="30 people">
                                        <span class="hidden-sm-and-down">>30 people</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 6"
                            >
                                Continue
                            </v-btn>
                            <v-btn text @click="e6=4">
                                Cancel
                            </v-btn>
                            </v-stepper-content>

                        <!-- step 6 -->
                            <v-stepper-step
                            :complete="e6 > 5"
                            step="6"
                            >
                           Select your oxygen level
                            </v-stepper-step>

                            <v-stepper-content step="6">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="oxygen"
                            mandatory
                                    color="cyan"
                                    borderless
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="95-100%">
                                        <span class="hidden-sm-and-down">95-100%</span>
                                    </v-btn>

                                    <v-btn value="90-95%">
                                        <span class="hidden-sm-and-down">90-95%</span>
                                    </v-btn>

                                    <v-btn value="80-85%">
                                        <span class="hidden-sm-and-down">80-85%</span>
                                    </v-btn>

                                    <v-btn value="< 80%">
                                        <span class="hidden-sm-and-down">< 80%</span>
                                    </v-btn>
                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 7"
                            >
                                Continue
                            </v-btn>
                            <v-btn text
                                @click="e6 = 5">
                                Back
                            </v-btn>
                            </v-stepper-content>
                            
                        <!-- step 7 -->
                            <v-stepper-step
                            :complete="e6 > 6"
                            step="7"
                            >
                           Select your current illness
                            </v-stepper-step>

                            <v-stepper-content step="7">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="illness"
                                    color="cyan"
                            mandatory
                                    borderless
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="none">
                                        <span class="hidden-sm-and-down">None</span>
                                    </v-btn>

                                    <v-btn value="diabetes">
                                        <span class="hidden-sm-and-down">Diabetes</span>
                                    </v-btn>

                                    <v-btn value="cancer">
                                        <span class="hidden-sm-and-down">Cancer</span>
                                    </v-btn>

                                    <v-btn value="obesity">
                                        <span class="hidden-sm-and-down">Obesity</span>
                                    </v-btn>

                                    <v-btn value="other">
                                        <span class="hidden-sm-and-down">Other Illness</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 8"
                            >
                                Continue
                            </v-btn>
                            <v-btn text
                                @click="e6 = 6">
                                Cancel
                            </v-btn>
                            </v-stepper-content>
                            
                        <!-- step 8 -->
                            <v-stepper-step
                            :complete="e6 > 7"
                            step="8"
                            >
                           Select your health protocol habit
                            </v-stepper-step>

                            <v-stepper-content step="8">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="protocol"
                            mandatory
                                    color="cyan"
                                    borderless
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="very good">
                                        <span class="hidden-sm-and-down">Very Good</span>
                                    </v-btn>

                                    <v-btn value="good">
                                        <span class="hidden-sm-and-down">Good</span>
                                    </v-btn>

                                    <v-btn value="Average">
                                        <span class="hidden-sm-and-down">Average</span>
                                    </v-btn>

                                    <v-btn value="Bad">
                                        <span class="hidden-sm-and-down">Bad</span>
                                    </v-btn>

                                    <v-btn value="Very Bad">
                                        <span class="Very Bad">Very Bad</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 9"
                            >
                                Continue
                            </v-btn>
                            <v-btn text
                                @click="e6 = 7">
                                Cancel
                            </v-btn>
                            </v-stepper-content>

                             <!-- step 9 -->
                            <v-stepper-step
                            :complete="e6 > 8"
                            step="9"
                            >
                           Have you been going abroad last 30 days?
                            </v-stepper-step>

                            <v-stepper-content step="9">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="abroad"
                                    color="cyan"
                                    borderless
                            mandatory
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="no">
                                        <span class="hidden-sm-and-down">No</span>
                                    </v-btn>

                                    <v-btn value="yes">
                                        <span class="hidden-sm-and-down">Yes</span>
                                    </v-btn>

                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="e6 = 10"
                            >
                                Continue
                            </v-btn>
                            <v-btn text
                                @click="e6 = 8">
                                Cancel
                            </v-btn>
                            </v-stepper-content>

                              <!-- step 10 -->
                            <v-stepper-step
                            :complete="e6 > 9"
                            step="10"
                            >
                           Did you already vaccinated?
                            </v-stepper-step>

                            <v-stepper-content step="10">
                            <div class="mb-5">
                                <v-btn-toggle
                                    v-model="vaccine"
                                    color="cyan"
                                    borderless
                            mandatory
                                    style="flex-flow:row wrap"
                                >
                                    <v-btn value="no">
                                        <span class="hidden-sm-and-down">No</span>
                                    </v-btn>

                                    <v-btn value="yes">
                                        <span class="hidden-sm-and-down">Yes</span>
                                    </v-btn>
                                    
                                </v-btn-toggle>
                            </div>

                            <v-btn
                                color="primary"
                                @click="predict()"
                            >
                                Start Predict
                            </v-btn>
                            <v-btn text
                               @click="restart()">
                                Restart
                            </v-btn>
                            </v-stepper-content>

                    </v-stepper>
                </div>
            </v-col>
            <v-col cols="12" md="6" lg="6" xl="6" class="visualArea no-gutters" :style="getStyleVisualArea">
                <div class="visualImg">
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender=='female'&&(output==''||output=='Not Infected')" src="~assets/img/women-very-low.png"/>
                    </v-fade-transition>
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender=='female'&&output=='Infected - High chance to recover'" src="~assets/img/women-high.png"/>
                    </v-fade-transition>
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender=='female'&&output=='Infected - Low chance to recover'" src="~assets/img/women-very-high.png"/>
                    </v-fade-transition>
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender!='female'&&(output==''||output=='Not Infected')" src="~assets/img/men-very-low.png"/>
                    </v-fade-transition>
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender!='female'&&output=='Infected - High chance to recover'" src="~assets/img/man-high.png"/>
                    </v-fade-transition>
                    <v-fade-transition leave-absolute hide-on-leave>
                        <img v-if="gender!='female'&&output=='Infected - Low chance to recover'" src="~assets/img/man-very-high.png"/>
                    </v-fade-transition>
                </div>
                <div class="infoArea" v-if="output=='Not Infected'">
                    <div class="infectionVal" style="background-color:#00db9a">
                        <span style="font-size:0.8em;">Prediction Result:</span> <br/>
                        <b style="font-size:1.2em">Not Infected</b>
                    </div>
                    <div class="white--text mt-5 px-5" style="font-size:0.8em">Our system predicted that you are <b>Not Infected</b>. Keep pyshical disntancing and wear your mask to reduce chance of getting infected. If you not feeling good someday please visit the nearest hospital here.<a href="https://www.google.com/maps/search/hospital" target="_blank">here</a>.</div>
                </div>
                <div class="infoArea" v-if="output=='Infected - High chance to recover'">
                    <div class="infectionVal"  style="background-color:#8c0000">
                        <span style="font-size:0.8em;">Prediction Result:</span> <br/>
                        <b style="font-size:1.2em;background-color:#8c0000">Infected - High change to recover</b>
                    </div>
                    <div class="white--text mt-5 px-5" style="font-size:0.8em">Our system predicted that you are <b>More likely Infected</b> by covid-19. Please visit the nearest hospital as soon as possible<a href="https://www.google.com/maps/search/hospital" target="_blank">here</a>.</div>
                </div>
                <div class="infoArea" v-if="output=='Infected - Low chance to recover'">
                    <div class="infectionVal" style="background-color:#8c0000">
                        <span style="font-size:0.8em;">Prediction Result:</span> <br/>
                        <b style="font-size:1.2em;">Infected - Low chance to recover</b>
                    </div>
                    <div class="white--text mt-5" style="font-size:0.8em">Our system predicted that you are <b>Infected</b> by covid-19. Please visit the nearest hospital as soon as possible<a href="https://www.google.com/maps/search/hospital" target="_blank">here</a>.</div>
                </div>
            </v-col>
        </v-row>

        <v-dialog
            v-model="dialog"
            persistent
            width="300"
            >
            <v-card style="padding:100px 10px;display:flex;alig-items:center;justify-content:center;" dark>
                <div class="text-center">
                <v-progress-circular :size="100" :width="20" indeterminate color="purple"></v-progress-circular>
                <div class="mt-10" >Generating Prediction Result</div>
                </div>
            </v-card>
    </v-dialog>

    </v-container fluid>
</template>

<script>
export default {
    data(){
        return {
            dialog:false,
            e6:1,
            gender:'female',
            age:'20-30',
            smoking:'no',
            chest:'no',
            people:'full isolation',
            oxygen:'95-100%',
            illness:'none',
            protocol:'very good',
            abroad:'no',
            vaccine:'yes',
            output:''
        }
    },
    methods:{
        restart(){
            this.e6=1
            this.output=''
        },
        predict(){
            this.dialog="true"
            setTimeout(()=>{
                this.dialog=false
                
                if(this.oxygen=='<80%'||this.oxygen=='80-85%'){
                    if(this.age=='>60'||this.age=='50-60'){
                        this.output = 'Infected - Low chance to recover'
                    }else{
                        this.output = 'Infected - High chance to recover'
                    }
                }else if(this.oxygen=='90-95%'){
                    if(this.age=='>60'||this.age=='50-60'){
                        if(this.chest=='almost every day' || this.chest=='almost every day and very sore'){
                            this.output = 'Infected - Low chance to recover'
                        }else{
                            this.output = 'Infected - High chance to recover'
                        }
                    }else{
                        if(this.chest=='almost every day and very sore'){
                            this.output = 'Infected - Low chance to recover'
                        }else{
                            this.output = 'Infected - High chance to recover'
                        }
                    }
                }else {
                    if(this.age=='>60'||this.age=='50-60'){
                        if(this.chest=='almost every day' || this.chest=='almost every day and very sore'){
                            this.output = 'Infected - Low chance to recover'
                        }else{
                            this.output = 'Infected - High chance to recover'
                        }
                    }else{
                        if(this.chest=='almost every day and very sore'){
                            this.output = 'Infected - High chance to recover'
                        }else{
                            this.output = 'Not Infected'
                        }
                    }
                }
                console.log(this.output)
            }, 2000);
        }
    },
    computed:{
        getStyleVisualArea:function(){   

            if(this.output=='Infected - High chance to recover'||this.output=='Infected - Low chance to recover'){
                return 'background: rgb(165,21,21);background: radial-gradient(circle, rgba(165,21,21,1) 0%, rgba(0,0,0,1) 63%)'
            }

            if(this.output=='Not Infected'){
                return 'background: rgb(13,145,141);background: radial-gradient(circle, rgba(13,145,141,1) 0%, rgba(0,0,0,1) 100%);'
            }
            
            if(this.output==''){
                return 'background: rgb(20,84,138);background: radial-gradient(circle, rgba(20,84,138,1) 0%, rgba(32,76,134,1) 0%, rgba(0,0,0,1) 100%)'
            }
  
            
        }
    }
}
</script>

<style lang="scss">

.visualArea {
  min-height: 100vh;
  padding-bottom:100px;
  display:flex;
  justify-content: center;
  align-items: center;
  position:relative;
  overflow:hidden
}

.infectionVal {
    color:#fff;
    padding:10px;
    font-size:1.5em;
    border-radius:20px;
    text-align:center;
    width:fit-content;
    min-width:300px;
}

.infoArea{
    position:absolute;
    bottom:30px;
    text-align:center;
    display:flex;
    flex-flow:column wrap;
    align-items:center;
    justify-content: center;
}

.questionArea {
    background: rgb(11,49,74);
    background: linear-gradient(95deg, rgba(11,49,74,1) 0%, rgba(26,9,37,1) 100%);
    height:100vh;
    overflow-y:scroll;
}

.visualImg{
    max-width:300px;
    position:absolute;

    img {
        width:100%;
    }
}

.appTitle {
    font-size:2em;
    background: rgb(38,156,255);
    background: linear-gradient(58deg, rgba(38,156,255,1) 0%, rgba(235,118,255,1) 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 900;
    line-height: 1;
}

.qsDivider {
    width:100%;height:1px;
    background: rgb(38,156,255);
    background: linear-gradient(58deg, rgba(38,156,255,1) 0%, rgba(235,118,255,1) 100%);
}

/* width */
::-webkit-scrollbar {
    width: 5px;
  }
  
  /* Track */
  ::-webkit-scrollbar-track {
    background: #000; 
  }
   
  /* Handle */
  ::-webkit-scrollbar-thumb {
    background: #313131; 
  }
  
  /* Handle on hover */
  ::-webkit-scrollbar-thumb:hover {
    background: #515151; 
  }
  
</style>