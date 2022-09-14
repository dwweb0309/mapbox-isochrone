<template>
  <div>
    <div id="map"></div>
  </div>
</template>

<script>
import Vue from 'vue'
import mapboxgl from '!mapbox-gl'
import 'mapbox-gl/dist/mapbox-gl.css'

export default Vue.extend({
  name: 'IndexPage',
  mounted() {
    mapboxgl.accessToken = 'pk.eyJ1IjoiZHd3ZWIwMzA5IiwiYSI6ImNsMWdjdWhxdDAxcXgzaWxubDlyYnV2b3YifQ.GbCstsimD2y-Oa1eQXfWDA'

    const map = new mapboxgl.Map({
      container: 'map',
      style: 'mapbox://styles/dwweb0309/cl1gd0tav006015ldem446se9',
      center: [151.209900, -33.865143],
      zoom: 12,
      hash: true
    })
  }
})
</script>

<style>
  #map {
    position: absolute;
    top: 0;
    bottom: 0;
    width: 100%;
  }
</style>