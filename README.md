# \<ability-chart\>

A canvas based ability chart component

## Preview
An easy to use and fully customizable ability chart web component based on Polymer 2.0.

## Usage
Add onto html just as normal tag elements. Use attribute `prop` to set up all the styles you want.

```html
<ability-chart prop='{
                  "eachPoint":[
	                  {"key":"Math", "value":85},
	                  {"key":"Physics", "value":30},
	                  {"key":"English", "value":55},
	                  {"key":"Chemistry", "value":100},
	                  {"key":"Chinese", "value":10},
	                  {"key":"History", "value":100}]}'>               	
</ability-chart>
```
## prop Options

prop Name | Description
--- | --- 
dimension | A number (i.e. 300). The height and width of the chart.
numLayer | A number (i.e. 3). The number of equally divided layers of the chart.
eachLayerStyle | An array of object (i.e. `{"fillColor: "#bf0a0a", ""borderColor": "#207476""}`).
labelFont | A css font string (i.e. "12px Arial"). The font of labels.
labelFontColor | A css color string (i.e. "black"). The color of labels.
fillColor | A css color string (i.e. "#d666c6"). The color of defined chart area.
borderColor | A css color string (i.e. "#d666c6"). The border color of defined chart area.
frameBorderWidth | A number (i.e. 1). The border width of the chart frame. 
chartBorderWidth | A number (i.e. 1). The border width of the defined chart.
decorLineColor | A css color string (i.e. "black"). The color of the center-to-vertex decoration lines.
chartPortion | A number (i.e. 0.7). The portion of the chart within the canvas. 
chartAlpha | A number (i.e. 0.7). The opacity of the defined chart.
eachPoint | An array of object (i.e. `{"key":"Strength", "value":30}`).

## License
MIT