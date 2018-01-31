<script>
import { Bar } from 'vue-chartjs'

const platformJSON = require('../assets/platform.json')

export default {
  name: 'graph',
  extends: Bar,
  data () {
    return {
      datacollection: {
        labels: ['January', 'February'],
        datasets: [
          {
            label: 'Data One',
            backgroundColor: '#f87979',
            data: [40, 20]
          },
          {
            label: 'Data One',
            backgroundColor: '#f87954',
            data: [10, 15]
          }
        ]
      }
    }
  },
  mounted () {
    console.info(platformJSON)
    this.renderChart(this.datacollection, {responsive: true, maintainAspectRatio: false})
  }
}

</script>
<!-- styling for the component -->
<style>
#bar-chart {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  width: 100% !important;
}
</style>
