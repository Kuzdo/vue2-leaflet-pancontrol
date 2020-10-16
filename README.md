# vue2-leaflet-pancontrol

This is a [Vue2Leaflet](https://github.com/vue-leaflet/Vue2Leaflet) plugin to provide the
[Leaflet.Pancontrol](https://github.com/kartena/Leaflet.Pancontrol) control
on [Leaflet](https://leafletjs.com/) maps in [Vue](https://vuejs.org/) applications.


## Installation
```bash
npm install --save vue2-leaflet-pancontrol
```

## Local demo
```bash
git clone git@github.com:kuzdo/vue2-leaflet-pancontrol.git
cd vue2-leaflet-pancontrol

npm install
npm run example
```
You should then be able to visit http://localhost:4000 to see a leaflet map with the pancontrol controls.


## Usage

### Adding the component to a map

With the `LControlPancontrol` component loaded into Vue (see below), simply add the
`l-control-pancontrol` element inside an `l-map`.
For example,
```html
<l-map>
  <l-control-pancontrol :position="'topright'" />
</l-map>
```

### Loading the Vue component

You can either install the control globally within your application at the point where you initially
configure Vue, or import the control only within the components that require it.


#### Option 1: Local import

In the `<script>` of a Vue component,
```js
import LControlPancontrol from 'vue2-leaflet-pancontrol';
// ...
export default {
  // ...
  components: {
    LControlPancontrol,
    // ...
  },
  // ...
};
```


#### Option 2: Global install

Where you load and configure your Vue environment,
```js
import Vue from 'vue';
import LControlPancontrol from 'vue2-leaflet-pancontrol';
// ...
Vue.component('l-control-pancontrol', LControlPancontrol);
// ...
```


## Credit

The majority of the credit for this plugin goes to the author of and contributors to the underlying
[Leaflet.Pancontrol control](https://github.com/kartena/Leaflet.Pancontrol), and of course
the plugin wouldn't be possible without Vue, Leaflet, and Vue2Leaflet.


### Plugin author

Przemysław Kużdowicz


## License

This project is licensed under the BSD 2-Clause "Simplified" License - see the [LICENSE](LICENSE) file for details.