# \<ability-chart\>

A canvas based ability chart component

## Preview
An easy to use and fully customizable ability chart web component based on Polymer 2.0.

## Usage
Add onto html just as normal tag elements. Pass a json object into the attribute `prop` to set up all the styles you want.

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
dimension | a number (i.e. `300`)<br>the height and width of the chart in px
numLayer | a number (i.e. `3`)<br>the number of equally divided layers of the chart
eachLayerStyle | an array of object (i.e. `{"fillColor: "#bf0a0a", ""borderColor": "#207476""}`)<br>`fillColor` is the color filled in the layer<br>`borderColor` is the border color of the layer
labelFont | a css font string (i.e. `"12px Arial"`)<br>the font of labels
labelFontColor | a css color string (i.e. `"black"`)<br>the color of labels
fillColor | a css color string (i.e. `"#d666c6"`)<br>the color of defined chart area
borderColor | a css color string (i.e. `"#d666c6"`)<br>the border color of defined chart area
frameBorderWidth | a number (i.e. `1`)<br>the border width of the chart frame
chartBorderWidth | a number (i.e. `1`)<br>the border width of the defined chart area
decorLineColor | a css color string (i.e. `"black"`)<br>the color of the center-to-vertex decoration lines
chartPortion | a number (i.e. `0.7`)<br>the portion of the chart within the canvas
chartAlpha | a number (i.e. `0.7`)<br>the opacity of the defined chart area
eachPoint | an array of object (i.e. `{"key":"Strength", "value":30}`)<br>`key` is the label of each vertex<br>`value` is the vertex value between 0 and 100

## Example
<!--
```
```
<custom-element-demo>
  <template>
    <link rel="import" href="ability-chart.html">
    <next-code-block></next-code-block>
  </template>
</custom-element-demo>
```
-->
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
## License
MIT