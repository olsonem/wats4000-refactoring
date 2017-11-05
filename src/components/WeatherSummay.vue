<template>
    <div>
        <div v-for="weatherSummary in weatherData" class="weatherSummary">
            <img v-bind:src="'http://openweathermap.org/img/w/' + weatherSummary.icon + '.png'" v-bind:alt="weatherSummary.main">
            <br>
            <b>{{ weatherSummary.main }}</b>
        </div>
    </div>
</template>
<script>
import {API} from '@/common/api';

export default {
  name: 'WeatherSummary',
  data () {
    return {

    }
  },
    props: {
        weatherData: []
    }
}
</script>
<style>

</style>
