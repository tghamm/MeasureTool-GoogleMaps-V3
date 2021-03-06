# Developer Guide
#### Dependency
Make sure the **`geometry`** library is referenced in the **Google Maps JavaScript API** loading script.
```html
libraries=geometry
```
#### Basic use
To create the measurement widget, pass in a Google Map instance.
```javascript
var measureTool = new MeasureTool(map);
```
#### Pass in `MeasureToolOptions`
You could also pass in a `MeasureToolOptions` as the second argument to customize to your preference. 
```javascript
var measureTool = new MeasureTool(map, {
  showSegmentLength: true,
  unit: MeasureTool.UnitTypeId.IMPERIAL // or just use 'imperial'
});
```
#### Bind to your own UI
The `MeasureTool` comes with a context menu out of box for saving your time to create your own. However, if you'd like to bind the `MeasureTool` to your own UI, you could specify `contextMenu` to `false` when constructing the `MeasureTool`. The `MeasureTool` exposes two public methods `start()` and `end()` to start and end measuring. For example,
```html
<button onclick="measureTool.start()">start</button>
<button onclick="measureTool.end()">end</button>
```
```javascript
var measureTool = new MeasureTool(map, {
  contextMenu: false
  // some other options...
});
```
