<template>
  <div>
    <div id="myChart" ref="myChart"></div>
  </div>
</template>

<script>
export default{
  name: 'chart',
  data () {
    return {
      chart: null,
      options: {}
    }
  },
  mounted () {
    this.initOptions()
    this.initCharts()
  },
  methods: {
    initOptions () {
      this.options = {
        title: {
          text: "测试表格"
        },
        tooltip: {
          trigger: 'axis'
        },
        xAxis: {
          type: 'category',
          data: ['Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat', 'Sun']
        },
        yAxis: {
          type: 'value'
        },
        series: [{
          data: [820, 932, 901, 934, 1290, 1330, 1320],
          type: 'line'
        }]
      }
    },
    initCharts () {
      // this.chart = this.$echarts.init(document.getElementById('myChart'))
      this.chart = this.$echarts.init(this.$refs.myChart)
      this.chart.setOption(this.options)
    }
  }
}
</script>

<style scoped>
  #myChart{
    width: 400px;
    height: 400px;
  }
</style>