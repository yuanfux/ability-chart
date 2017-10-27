# \<ability-chart\>
[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/yuanfux/ability-chart)

A canvas based ability chart component

## Preview
An easy to use and fully customizable ability chart web component based on Polymer 2.0.

![img broken](/demoImg/demo1.png "ability-chart demo1")

![img broken](/demoImg/demo2.png "ability-chart demo2")

![img broken](/demoImg/demo3.png "ability-chart demo3")

## Usage
Add onto html just as normal tag elements. Pass a json object into the attribute `prop` to set up all the styles you want.
<!--
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
## prop Options

prop Name | Description | Default
--- | --- 
dimension | a number (i.e. `300`)<br>the height and width of the chart in px | `300`
numLayer | a number (i.e. `3`)<br>the number of equally divided layers of the chart | `1`
eachLayerStyle | an array of object (i.e. `{"fillColor: "#bf0a0a", ""borderColor": "#207476""}`)<br>`fillColor` is the color filled in the layer<br>`borderColor` is the border color of the layer | `null`
labelFont | a css font string (i.e. `"12px Arial"`)<br>the font of labels | `"12px Arial"`
labelFontColor | a css color string (i.e. `"black"`)<br>the color of labels | `null`
fillColor | a css color string (i.e. `"#d666c6"`)<br>the color of defined chart area | `null`
borderColor | a css color string (i.e. `"#d666c6"`)<br>the border color of defined chart area | `null`
frameBorderWidth | a number (i.e. `1`)<br>the border width of the chart frame | `null`
chartBorderWidth | a number (i.e. `1`)<br>the border width of the defined chart area | `null`
decorLineColor | a css color string (i.e. `"black"`)<br>the color of the center-to-vertex decoration lines | `null`
chartPortion | a number (i.e. `0.7`)<br>the portion of the chart within the canvas | `0.85`
chartAlpha | a number (i.e. `0.7`)<br>the opacity of the defined chart area | `null`
eachPoint | an array of object (i.e. `{"key":"Strength", "value":30}`)<br>`key` is the label of each vertex<br>`value` is the vertex value between 0 and 100 | `null`

## Example
Here is a fully customized example. For more examples, check out demo in the repo.
```html
<ability-chart prop='{
                    "dimension": 500, 
                    "numLayer": 5,
                    "eachLayerStyle":[
		                {
		                  "fillColor":"#bf0a0a",
		                  "borderColor": "#207476"
		                }, 
		                {
		                  "fillColor":"#ff6161",
		                  "borderColor": "#ffdba2"
		                }, 
		                {
		                  "fillColor":"#ffafa2",
		                  "borderColor": "#ffafa2"
		                },
		                {
		                  "fillColor":"#ffdba2",
		                  "borderColor": "#ff6161"
		                }, 
		                {
		                  "fillColor":"#ffffff",
		                  "borderColor": "#bf0a0a"
		                }],
	                "labelFont": "13px Arial",
	                "labelFontColor":"red",
	                "fillColor":"#ffc125",
	                "frameBorderWidth": 2,
	                "chartBorderWidth": 2,
	                "borderColor": "#207476",
	                "decorLineColor": "#207476",
	                "chartPortion": 0.8,
	                "chartAlpha": 0.5,
	                "eachPoint":[
	                    {"key":"Strength", "value":85},
		                {"key":"Stamina", "value":39},
		                {"key":"Perception", "value":55},
		                {"key":"Creativity", "value":77},
		                {"key":"Charisma", "value":95},
		                {"key":"Confidence", "value":84},
		                {"key":"Spirituality", "value":50},
		                {"key":"Discipline", "value":90},
		                {"key":"Luck", "value":69},
		                {"key":"Humor", "value":80},
		                {"key":"Social Skill", "value":30}]}'> 
</ability-chart>
```
## License
MIT