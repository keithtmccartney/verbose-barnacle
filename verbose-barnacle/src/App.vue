<template>
  <div id="app">
    <dashboard-content :highlights="highlights" :tempVar="tempVar"></dashboard-content>

    <div id="search">
      <input id="location-input" type="text" ref="input" placeholder="Location?" @keyup.enter="organizeAllDetails">

      <button id="search-btn" @click="organizeAllDetails">
        <img src="./assets/Search.svg" width="24" height="24">
      </button>
    </div>

    <div id="info">
      <div class="wrapper-left">
        <div id="current-weather">
          {{ currentWeather.temp }}
          <span>°C</span>
        </div>
        <div id="weather-desc">
          {{ currentWeather.summary }}
        </div>
        <div class="temp-max-min">
          <div class="max-desc">
            <div id="max-detail">
              <i>▲</i>
              {{ currentWeather.todayHighLow.todayTempHigh }}
              <span>°C</span>
            </div>
          </div>
        </div>
        <div id="max-summary">
          at {{ currentWeather.todayHighLow.todayTempHighTime }}
        </div>
        <div class="min-desc">
          <div id="min-detail">
            <i>▼</i>
            {{ currentWeather.todayHighLow.todayTempLow }}
            <span>°C</span>
          </div>
          <div id="min-summary">
            at {{ currentWeather.todayHighLow.todayTempLowTime }}
          </div>
        </div>
      </div>
      <div class="wrapper-right">
        <div class="date-time-info">
          <div id="date-desc">
            <img src="./assets/calendar.svg" width="20" height="20">
            {{ currentWeather.time }}
          </div>
        </div>
        <div class="location-info">
          <div id="location-desc">
            <img src="./assets/location.svg" width="10.83" height="15.83" style="opacity: 0.9;">
            {{ currentWeather.full_location }}
            <div id="location_detail" class="mt-1">
              Lat: {{ currentWeather.formatted_lat }}
              <br>
              Long: {{ currentWeather.formatted_long }}
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  // import statements here
  // import Content from './components/Content.vue'

  export default {
    // name, components, props, etc.
    // name: 'app',
    // components: {
    //   'dashboard-content': Content
    // },
    data () {
      return {
        // the data that is so crucial for the application is defined here.
        // the data objects will have certain default values chosen by us.
        // The methods that we define below will manipulate the data.
        // Since the data is bounded to various attributes and directives, they
        // will update as and when the values of the data objects change.

        // tempVar: {
        //   tempToday: [
        //     {hour: '11.00 AM', temp: '35'},
        //     {hour: '12.00 PM', temp: '36'},
        //     {hour: '1.00 PM', temp: '37'},
        //     {hour: '2.00 PM', temp: '38'},
        //     {hour: '3.00 PM', temp: '36'},
        //     {hour: '4.00 PM', temp: '35'},
        //   ],
        // },
        // highlights: {
        //   uvIndex: 4,
        //   visibility: 10,
        //   windStatus: {
        //     windSpeed: '30 km/h',
        //     windDirection: '30',
        //     derivedWindDirection: 'NNE',
        //   },
        // },
      }
    },
    methods: {
      // methods (objects whose values are functions) here.
      // bulk of dynamic stuff (the black magic part) is controlled from here.
    },
    computed: {
      // computed properties here
    },
    // other objects, as necessary
}
</script>

<style>
</style>
