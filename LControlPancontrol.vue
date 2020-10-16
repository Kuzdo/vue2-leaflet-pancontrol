<script>
import {OptionsMixin, ControlMixin, propsBinder, optionsMerger } from "vue2-leaflet";
import LeafletPancontrol from "leaflet.pancontrol";
import 'leaflet.pancontrol/src/L.Control.Pan.css'

export default {
  name: 'LControlPancontrol',
  mixins: [
      ControlMixin,
      OptionsMixin,
  ],
  mounted() {
    const options = optionsMerger({
      ...this.controlOptions,
      options: this.options,
    }, this);
    this.mapObject = new LeafletPancontrol(options);
    propsBinder(this, this.mapObject, this.$options.props);
    this.mapObject.addTo(this.$parent.mapObject);
  },
  render() {
    return null;
  },
};
</script>
