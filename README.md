# tcg-comparison-widget

This is a re-usable Polymer 0.5.* comparison element that can be used to display a main metric and compare it against 
at least 1 other metric; it is configurable for up to 2 more optional metrics to be compared against. Clicking the
element will bring the graph to full-screen wheres comparisons and details are displayed in full.

### How to install

```
bower install --save tcg-comparison-widget
```

## How to use
###Include the element in your page

```
<link rel="import" href="/bower_components/tcg-comparison-element/tcg-comparison-element.html">
```

###Then use the element in your page

```
<tcg-comparison-widget chart-data-categories="['01', '02', '03', '04', '05', '06', '07']"
                    chart-data-series="[{'name': 'Realtime Users', 'data': [500, 1000, 3000, 4000, 3000, 2000, 1700]}]"
                    chart-data-selected="[5]"
                    chart-data-trendline="2000"
                    chart-line-colors="['#fff', '#acacac']" chart-line-styles="['Solid']"
                    chart-x-axis-gridline-color="rgba(0, 0, 0, .1)" chart-trendline-color="rgba(255, 255, 255, .2)"
                    chart-x-axis-text-color="#fff" chart-y-axis-text-color="#fff"
                    chart-tooltip-format="0,0"
                    enable-menu-action="true"
                    enable-transpose-action="true">
  <tcg-comparison-widget-main-metric
    label="REALTIME USERS"
    stat="0"
    ></tcg-comparison-widget-main-metric>
  <tcg-comparison-widget-metric
    label="YESTERDAY"
    stat="0"
    compare-to="0"
    format="0,0"
    ></tcg-comparison-widget-metric>
  <tcg-comparison-widget-metric
    label="LAST WEEK"
    stat="0"
    compare-to="0"
    ></tcg-comparison-widget-metric>
  <tcg-comparison-widget-metric
    label="LAST MONTH"
    stat="0"
    compare-to="0"
    ></tcg-comparison-widget-metric>
  <transposed-content>
    Transposed Content
  </transposed-content>
</tcg-comparison-widget>
```
