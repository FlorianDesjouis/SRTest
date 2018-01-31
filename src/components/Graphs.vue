<script>
import { Bar } from 'vue-chartjs'
import $ from 'jQuery'

export default {
  name: 'graph',
  extends: Bar,
  data () {
    return {
      labels: null
    }
  },
  mounted () {
    this.getJSON()
    this.renderChart()
  },
  methods: {
    getJSON: function () {
      $.getJSON('./assets/platform.json', (json) => {
        this.labels = json.map(function (item) {
          return item.platform
        })
      })
    },
    renderChart: function (labels, datasets) {
      console.info(this.labels)
      labels: this.labels
      datasets: [
        {
          label: 'Platform used',
          backgroundColor: '#f87979',
          data: [40, 20, 12, 39, 10, 40, 39, 80, 40, 20, 12, 11]
        }
      ]
      // ici fait ce que tu veux avec le label
    }
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
