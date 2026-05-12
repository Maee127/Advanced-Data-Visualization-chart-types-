# Advanced-Data-Visualization-chart-types-
A complete guide to choose a chart to show data;
Show types of chart to show data relationship on Iris & World Population datasets
## Quick Decision Flowchart to choose a chart:
What's your goal?
│
├─ Show RELATIONSHIPS between variables
│  ├─ 3 numerical variables → 3D Scatter (#1)
│  └─ 3 variables (x, y, size) → Bubble (#4)
│
├─ Show DISTRIBUTION of one variable
│  └─ Histogram (#2)
│
├─ Show COMPOSITION (parts of a whole)
│  ├─ Simple 2-5 categories → Pie/Donut (#3)
│  ├─ Hierarchical categories → Sunburst (#5)
│  └─ Over time → Area Chart (#10)
│
├─ Show PROGRESS toward a goal
│  └─ Gauge (#6)
│
├─ Show POPULATION demographics
│  └─ Pyramid (#7)
│
├─ Show CONVERSION or sequential loss
│  └─ Funnel (#8)
│
└─ Show CHANGE OVER TIME
   ├─ To impress/storytell → Animated Bar (#9)
   └─ For cumulative view → Area (#10)

## Pro tips:
Chart	              Pro Tip
3D Scatter	        Use Plotly (interactive) — Matplotlib 3D is hard to rotate. Limit to 3-4 color groups.
Histogram	          Try nbins=20-30. Add KDE overlay for smoother view. Use marginal='box' in Plotly.
Pie/Donut	          Never use for >5 categories. Donut (hole=0.4) is more modern than pie. Sort slices by size.
Bubble	            Set size_max=40 to avoid giant bubbles. Add opacity for overlap. Consider log scales.
Sunburst	          Max 3-4 hierarchy levels. Use textinfo='label+percent parent' for clarity.
Gauge	              Only for dashboards/KPIs. Not for detailed analysis. Use Plotly go.Indicator.
Pyramid	            Classic for census data. Left=male, right=female is the convention.
Funnel	            Values must decrease! If they increase, use a bar chart instead.
Animated Bar	      Export as GIF for LinkedIn. Keep top 10-15 categories max. Add year label.
Area Chart	        Stacked version shows composition. Use groupnorm='percent' for 100% stacked view.
