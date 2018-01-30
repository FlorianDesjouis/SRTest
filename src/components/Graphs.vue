<script>
import { Bar, Line } from 'vue-chartjs'

$.getJSON('./assets/platform.json', function(json){
  var labels = json.map(function(item){
    return item.platform
  })
})

export default {
  name: 'graph',
  extends: Bar,
  mounted () {
    // Overwriting base render method with actual data.
    this.renderChart({
      labels: labels,
      datasets: [
        {
          label: 'Platform used',
          backgroundColor: '#f87979',
          data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11]
        }
      ]
    })
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
