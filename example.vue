<template>
  <div style="height: 100vh; width: 100%;">
    <l-map
        style="height: 100%"
        :center="mapCentre"
        :zoom="mapZoom"
        ref="map"
    >
      <l-tile-layer
          :url="tileUrl"
          :attribution="tileAttribution"
      />
      <l-control-pancontrol :position="'topright'"/>
    </l-map>
  </div>
</template>

<script>
import {LMap, LTileLayer} from "vue2-leaflet";
import LControlPancontrol from "./LControlPancontrol.vue";

export default {
  components: {
    LMap,
    LTileLayer,
    LControlPancontrol,
  },
  data() {
    return {
      mapCentre: [51.94, 15.50],
      mapZoom: 14,
      tileUrl: 'https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png',
      tileAttribution: '&copy; <a href="//osm.org/copyright">OpenStreetMap</a> contributors',
    }
  },
};
</script>

<style>
@import '~reset-css';
@import '~leaflet/dist/leaflet.css';
</style>