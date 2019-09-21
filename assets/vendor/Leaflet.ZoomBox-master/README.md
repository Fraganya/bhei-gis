# Leaflet.ZoomBox

A zoom box control for Leaflet.  

It allows you to draw an area on the map to zoom into.  See the [example](http://consbio.github.io/Leaflet.ZoomBox).

*Tested with Leaflet 1.1.*


## Install

From NPM:

```
npm install leaflet-zoombox
```


## Usage

Include the CSS: 

```
<link rel="stylesheet" href="L.Control.ZoomBox.css" />
```


Include the JavaScript:

```
<script src="L.Control.ZoomBox.min.js"></script>
```


This control uses [Google Material Icons](https://design.google.com/icons) by default.



Example usage:

```
var options = {
    modal: true,
    title: "Box area zoom"
};
var control = L.control.zoomBox(options);
map.addControl(control);
```
Options:
- *modal*: (boolean, default = `false`); if false, it deactivates after each use; if true, zoomBox control stays active until you click on the control again to deactivate options (like a toggle button)
- *position*: (string, default = `"topleft"`); position of the control
- *title*: (string, default = `"Zoom to specific area"`) title attribute for the control
- *className*: (string, default = `"leaflet-zoom-box-icon"`) className of the control link, which you can use to override the default styling; the `active` class will also be toggled for this element, when the control is activated; you can also override the control container style by creating a new CSS rule for `.leaflet-zoom-box-control`
- *content*: (string, default = `""`) html content to set as `innerHTML` of the control link; used in conjunction with the *className* option, you can use svg or html code to customize the control (see **[examples/customContent.html](http://consbio.github.io/Leaflet.ZoomBox/examples/customContent.html)**)
- *addToZoomControl*: (bool, default = `false`) if true, it will attempt to add the control to the map's existing zoomControl container; if false, the control link will be placed in a its own container


## Changes:
* `leaflet-zoom-box-icon` className is now used for the control link; use of `leaflet-zoom-box-control a {...}` to style the control link in the CSS has been removed. 


## Credits:
Developed with support from the [South Atlantic Landscape Conservation Cooperative](http://www.southatlanticlcc.org/), and maintained with support from [Peninsular Florida LCC](http://peninsularfloridalcc.org/) and the [U.S. Forest Service Northwest Regional Climate Hub](http://www.fs.fed.us/climatechange/nrch/).

Binding to the map's zoom box (shift-click) was inspired by [ScanEx](https://github.com/ScanEx/gmxControls/blob/master/examples/L.Control.boxZoom.html)


## Contributors:
* [Brendan Ward](https://github.com/brendan-ward)
* [Nik Stevenson-Molnar](https://github.com/nikmolnar)
* [Kaveh Karimi-Asli](https://github.com/ka7eh)
* [Andreas Adelsberger](https://github.com/punknroll)
* [Isaac Nygaard](https://github.com/azmisov)


## See Also:
[L.Control.BoxZoom](https://github.com/gregallensworth/L.Control.BoxZoom): an alternative implementation
