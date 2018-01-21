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
<ability-chart prop='
                  {
                     "datasets":{
                       "keys": ["Math", "Physics", "Physics", "Chemistry", "Chinese", "History"],
                       "values": [[85, 30, 55, 100, 10, 100]]
                     }
                  }'>
</ability-chart>
```
## prop Options

prop Name | Description | Type | Example | Default
--- | --- | --- | --- | ---
prop.dimension | the height and width of the chart in px | Number | `300` | `300`
prop.numLayer | the number of equally divided layers of the chart<br> must be defined if scale label needs to be shown | Number | `1`| `1`
prop.eachLayerStyle | an array of object defines each layer style)| Array<Object> | `[{"fillColor": "#bf0a0a", ""borderColor": "#207476""}]` | -
prop.eachLayerStyle.fillColor | the color of layer area | String | `"#d666c6"` | -
prop.eachLayerStyle.borderColor | the border color of layer area | String | `"#d666c6"` | -
prop.scale | an object defines the scale labels | Object |`"scale": {"font": "bold 12px Arial", "fontColor": "black", "offset": 12, "scaleLabel": ["0", "20", "40"]}` | -
prop.scale.font | the font of scale label | String | `"12px Arial"` | -
prop.scale.fontColor | the color of scale labels | String | `"#d666c6"` | -
prop.scale.offset | the offset of scale labels | Number | `5` | -
prop.scale.scaleLabel | the texts of scale labels (array length has to be `prop.numLayer + 1`)| Array<String> | `["0", "20", "40"]` | -
prop.labelFont | the font of labels | String | `"12px Arial"` | `"12px Arial"`
prop.labelFontColor | the color of labels | String | `"#d666c6"` | -
prop.labelOffset | the offset of labels | Numebr | `5` | -
prop.frameBorderWidth | the border width of the chart frame | Number | `1` | -
prop.chartBorderWidth | the border width of the defined chart area | Number | `1` | -
prop.decorLineColor | the color of the center-to-vertex decoration lines | String | `"#d666c6"` | -
prop.chartPortion | the portion of the chart within the canvas | Number | `0.85` | `0.85`
prop.chartAlpha | the opacity of the defined chart area | Number | `0.5` | -
prop.datasets | an object defines the data, data labels and data styles | Object |`"datasets": {"keys": ["Leadership", "Teamwork", "Management", "Visionary"], "values": [[79, 35, 55, 89]], "styles": [{"fillColor":"#ea9513", "borderColor": "#ea9513"}]}` | -
prop.datasets.keys | the labels of the chart | Array<String> | `["Leadership", "Teamwork", "Management", "Visionary"]` | -
prop.datasets.values | the data of the chart | Array<Array<Number>> | `[[79, 35, 55, 89]]` | -
prop.datasets.styles | the styles of datasets | Array<Object> | `[{"fillColor":"#ea9513", "borderColor": "#ea9513"}]` | -
prop.datasets.styles.fillColor | the color of a chart data area | String | `"#ea9513"` | -
prop.datasets.styles.borderColor | the border color of a chart data area | String | `"#ea9513"` | -

## Example
Here is a fully customized example. For more examples, check out demo in the repo.
```html
<ability-chart prop='{
                "dimension": 500,
                "numLayer": 5,
                "eachLayerStyle":[
                {
                  "fillColor":"#f5f5f5",
                  "borderColor": "#bbbbbb"
                },
                {
                  "fillColor":"#e6e6e6",
                  "borderColor": "#bbbbbb"
                },
                {
                  "fillColor":"#f5f5f5",
                  "borderColor": "#bbbbbb"
                },
                {
                  "fillColor":"#e6e6e6",
                  "borderColor": "#bbbbbb"
                },
                {
                  "fillColor":"#f5f5f5",
                  "borderColor": "#bbbbbb"
                }],
                "labelFont": "13px Arial",
                "labelFontColor":"#7a7a7a",
                "labelOffset": 10,
                "frameBorderWidth": 1,
                "chartBorderWidth": 2,
                "decorLineColor": "#bbbbbb",
                "chartPortion": 0.75,
                "chartAlpha": 0.95,
                "scale": {
                  "font": "bold 12px Arial",
                  "fontColor": "black",
                  "offset": 12,
                  "scaleLabel": ["0", "20", "40", "60", "80", "100"]
                },
                "datasets":
                  {
                    "keys": [
                              "Strength", "Stamina", "Perception",
                              "Creativity", "Charisma", "Confidence",
                              "Spirituality", "Discipline", "Luck", "Humor",
                              "Social Skill"
                            ],
                    "values": [[85, 39, 55, 77, 95, 84, 50, 90, 69, 80, 30],
                               [30, 70, 5, 100, 86, 30, 60, 100, 77, 33, 18]],
                    "styles": [{"borderColor": "#334b5c"}, {"borderColor": "#d53c37"}]
                  }
                }'>
</ability-chart>
```
## License
MIT
