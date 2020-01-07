---
layout: page
show_title: false
banner:
  collection: eyreville
  pid: obj03
  y: 25%
  height: '500px'
---
### Eyreville (44NH0507) is an archaeological site on Virginia's Eastern shore.  


{% raw %}
<div id="map" class="map leaflet-container" style="height: 500px; position:relative;"></div>
{% endraw %}


{% raw %}
<!-- <script>
  $.getJSON("/search/index.json", function(json_store) {
   // create elasticlunr index
    window.index = new elasticlunr.Index;
    window.store = json_store;
    index.saveDocument(false);
    index.setRef('lunr_id');
    index.addField('title');
    index.addField('coordinates');
    index.addField('link');
    index.addField('thumbnail');
    index.addField('lat');
    index.addField('lon');

    console.log(store.length);
    // add docs
    for (i in store) {
      var doc = elasticlunrRanges.splitCoords(store[i]);
      doc['lunr_id'] = i;
      index.addDoc(doc);
    }

    // map and tile layer
    window.map_viewer;
    map_viewer = L.map('map-viewer', {
      center: [39.44,-98.70],
      zoom: 4
    });
    L.tileLayer('https://stamen-tiles-{s}.a.ssl.fastly.net/terrain-background/{z}/{x}/{y}.{ext}', {
    	attribution: 'Map tiles by <a href="http://stamen.com">Stamen Design</a> &mdash; Map data &copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
    	subdomains: 'abcd',
    	minZoom: 0,
    	maxZoom: 18,
    	ext: 'png'
    }).addTo(map_viewer);
    L.tileLayer('https://stamen-tiles-{s}.a.ssl.fastly.net/toner-labels/{z}/{x}/{y}.{ext}', {
      attribution: 'Map tiles by <a href="http://stamen.com">Stamen Design</a> &mdash; Map data &copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>',
      subdomains: 'abcd',
      minZoom: 0,
      maxZoom: 18,
      ext: 'png'
    }).addTo(map_viewer);

    // markers
    elasticlunrRanges.placeMarkers(map_viewer, index, store);
    elasticlunrRanges.decorateMap(map_viewer, index, store);
  });
  $('.map-link').click(function(){
    console.log('here');
    var coordinate = $(this).attr('data-coordinate').split(",");
    map_viewer.setView(coordinate, 12);
  });
</script> -->


<!-- <script>
// create the map object and set the cooridnates of the initial view:
var map = L.map('map').setView([37.33681, -76,96358], 11);
var customLayer = L.geoJson(null, {
  onEachFeature: function(feature, layer) {
    layer.bindPopup(feature.properties.pid);
    }
});
var runLayer = omnivore.csv('.../\_data/eyreville.csv', null, customLayer)


// create the tile layer with correct attribution:
L.tileLayer('http://{s}.tiles.mapbox.com/v3/jamesg87.goac2bf1/{z}/{x}/{y}.png', {
    attribution: 'Map data &copy; <a href="http://openstreetmap.org">OpenStreetMap</a> contributors, <a href="http://creativecommons.org/licenses/by-sa/2.0/">CC-BY-SA</a>, Imagery © <a href="http://mapbox.com">Mapbox</a>',
    maxZoom: 18

  }).addTo(map);
</script>
{% endraw %} -->

This is a website made by Jolene Smith purely for experimentation and demonstration using __Wax__, a [tool](https://minicomp.github.io/wiki/#/wax/) for generating static sites for digital humanities using principles of Minimal Computing.

The collection items are taken from my colleagues at DHR, but much of the attribute data is invented for the demo.

### Browse the Collection

{% include collection_gallery.html facet_by='object_type' collection='eyreville' %}
