<template>
  <div class="line-chart-container">
    <div v-if="infor.length != 0">
      <D3LineChart :config="config" :datum="infor"></D3LineChart>
    </div>
  </div>
</template>

<script>
/*
import * as d3 from "d3";
import numeral from "numeral";
import { getCountryTimeline } from "@/services/corona-api";
import ToggleButton from "@/components/common/ToggleButton";

import Raphael from 'raphael/raphael'
global.Raphael = Raphael
 
import { LineChart } from 'vue-morris'
*/
import {D3LineChart} from 'vue-d3-charts'

export default {
  name: "Graph",
  props: {
    infor: Array
  },
  components: {
   D3LineChart
  },
  data(){
    return{
      config: {
                    values: ["val"],
                    date: {
                      key: 'year',
                      inputFormat: '%Y',
                      outputFormat: '%Y',
                    },
                    points:true,
                    axis: {
                      yTicks: 10,
                      xTicks: 20
                    }
                  }   
    }
  }
  
  
}
</script>

