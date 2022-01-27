# L.switchBasemap
An easy leaflet plugin to switch basemap

![image](https://user-images.githubusercontent.com/57905996/151415980-efef5fd8-6a97-4a05-b69c-cfd09c830edc.png)


Based and inspired on [Leaflet-IconLayers](https://github.com/ScanEx/Leaflet-IconLayers)

### [DEMO](https://elegant-meninsky-515912.netlify.app)

-----------------------------------------------------------------------------------
## Requirements

<ul>
  <li>Leaflet</li>
</ul>

## Install

### NPM

```
npm i leaflet-switch-basemap
```  

## Usage Example

An easy way to implement control to switch between basemaps

```javascript
new L.basemapsSwitcher([
  {
    layer: L.tileLayer('http://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '&copy; <a href="https://www.openstreetmap.org/copyright">OpenStreetMap</a> contributors'
    }).addTo(map), //DEFAULT MAP
    icon: './assets/images/img1.PNG',
    name: 'Map one'
  },
  {
    layer: L.tileLayer('https://tiles.stadiamaps.com/tiles/alidade_smooth/{z}/{x}/{y}{r}.png',{
      attribution: '&copy; <a href="https://stadiamaps.com/">Stadia Maps</a>, &copy; <a href="https://openmaptiles.org/">OpenMapTiles</a> &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors'
    }),
    icon: './assets/images/img2.PNG',
    name: 'Map two'
  },
  {
    layer: L.tileLayer('http://{s}.tile.stamen.com/toner-lite/{z}/{x}/{y}.png', {
      attribution: 'Map tiles by <a href="http://stamen.com">Stamen Design</a>, <a href="http://creativecommons.org/licenses/by/3.0">CC BY 3.0</a> &mdash; Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, <a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>'
    }),
    icon: './assets/images/img3.PNG',
    name: 'Map three'
  },
], { position: 'topright' }).addTo(map);

```
L.switchBasemap receives two arguments:
<ul>
  <li>The first is an array of objects that contains basemap configs</li>
  <li>The second is an object with control options</li>
</ul>

### Basemap config

| Property | Type   | Required  | Description                         |
| ------------|--- | -------- | ----------------------------------------- |
| layer     | Leaflet layer | true     | A leaflet layer that can be used as basemap (example: L.tileLayer)            |
| icon | String |true| Path of the Image that will be display on the control |
| name | String  | true | Name of the layer |

### Options
| Option	  | Type | Default  | Description                       |
| ------------|--- | -------- | ----------------------------------------- |
| position	  |String | 'topright'    | Position of the control. Options: [leaflet control positions](https://docs.eegeo.com/eegeo.js/v0.1.665/docs/leaflet/L.Control/#control-positions) |
