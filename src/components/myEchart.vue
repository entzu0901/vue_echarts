<template>
  <div :id="uuid" :style="style">
      Echarts
  </div>
</template>

<script>
import * as echarts from 'echarts'
const id=()=>{
    return new Date().getTime()
}
export default {
    name:'myEchart',
    props:{
        height:{
            type:String,
            default:'400px'
        },
        width:{
            type:String,
            default:'600px'
        }
    },
    computed:{
        style(){
            return{
                height:this.height,
                width:this.width
            }
        }
    },
    data() {
        return {
            uuid:null,
            myChart:null
        }
    },
    created(){
        this.uuid=id()
    },
    mounted() {
        this.myChart = echarts.init(document.getElementById(this.uuid));
        var option = {
        title: {
          text: 'ECharts 入门示例'
        },
        tooltip: {},
        legend: {
          data: ['销量']
        },
        xAxis: {
          data: ['衬衫', '羊毛衫', '雪纺衫', '裤子', '高跟鞋', '袜子']
        },
        yAxis: {},
        series: [
          {
            name: '销量',
            type: 'bar',
            data: [5, 20, 36, 10, 10, 20]
          }
        ]
      };
    this.myChart.setOption(option);
 }
}
</script>

<style>

</style>