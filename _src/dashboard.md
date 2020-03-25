---
nav: Dashboard
---

<div class="dashboard">
  <div class="title-container">
    <h1 class="title">Visual dashboard</h1>
  </div>
  <div class="map-container">
    <div class="map-column">
      <h2>Cases per one million people</h2>
      <div id="map-legend"></div>
      <div class="map" title="State Positive Cases / million people" id="state-map"></div>
    </div>
  </div>
  <p class="a11y-only"><a href="/data">Access data by state</a></p>  <div class="side-by-side">
    <div class="graphic" id="chart-daily-positive-total"></div>
    <div class="graphic" id="chart-daily-death-total"></div>
  </div>
  <div id="chart-state-small-multiples">
    <h3 class="chart-hed">Cumulative tests per state</h3>
    <p class="chart-dek">We track <span id="small-multiples-positive-span">positive</span> and <span id="small-multiples-total-span">total</span> tests per state, each day.</p>
    <div class="charts"><!-- where the graphics end up --></div>
    <div class="charts-notes">
      <p><strong>Note:</strong> We derive the <code>total</code> value by adding together the <code>positive</code> and <code>negative</code> value for each state. This is to account for differences in how states reporting <code>pending</code> tests.</p>
    </div>
  </div>
</div>

<script src="/_assets/js/d3.js"></script>
<script src="/_assets/js/d3-legend.js"></script>
<script src="/_assets/js/britecharts.js"></script>

<!-- map resources -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.6.0/dist/leaflet.css"
   integrity="sha512-xwE/Az9zrjBIphAcBb3F6JVqxf46+CDLwfLMHloNu6KEQCAWi6HcDUbeOfBIptF7tcCzusKFjFw2yuvEpDL9wQ=="
   crossorigin=""/>
<script src="https://unpkg.com/leaflet@1.6.0/dist/leaflet.js"
   integrity="sha512-gZwIG9x3wUXg2hdXF6+rVkLF/0Vi9U8D2Ntg4Ga5I5BZpVkVxlJWbSQtXPSiUTtC0TjtGOmxa1AJPuV0CPthew=="
   crossorigin=""></script>
<script src="https://cdn.jsdelivr.net/npm/@turf/turf@5/turf.min.js"></script>

<!-- scripts below are for Albers US map projections (currently unused) -->
<!--
<script src="https://unpkg.com/proj4leaflet@1.0.2/src/proj4leaflet.js"></script>
<script src="https://unpkg.com/proj4@2.6.0/dist/proj4-src.js"></script>
-->

<link rel="stylesheet" href="/_assets/css/_dashboard.css" >
<script src="/_assets/js/dashboard-charts.js"></script>
<script src="/_assets/js/dashboard-map.js"></script>