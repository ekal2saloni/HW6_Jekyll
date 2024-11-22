# Building Inventory Dataset Visualisations
*Submitted By Saloni Ekal (ekal2@illinois.edu)*
 
 
## Visualization 1: Bar Chart of Average Square Footage by Usage Description
<div id="vis1"></div>
 
<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
 
<script>
  // Load the JSON specification for Visualization 1
  vegaEmbed('#vis1', 'bar_chart.json').catch(console.error);
</script>
 
**Writeup:**

This bar chart visualizes the average square footage of buildings categorized by their usage descriptions, providing insights into how space is allocated across different building types. The x-axis encodes the average square footage (quantitative), and the y-axis encodes the usage description (nominal). A sequential color scheme is used, where each usage type is assigned a distinct color to improve visual distinction, though no ordinal relationship exists between categories. The dataset was grouped by the Usage Description column, and the mean of the Square Footage was calculated, while missing values were removed to ensure accurate data representation. This plot builds on similar grouping methods from Homework #5 but is created using Altair, requiring additional data transformation steps such as handling row limits and preparing the dataset with Pandas.
 
 
## Visualization 2 : Interactive Scatter Plot of Square Footage vs. Year Acquired
<div id="vis2"></div>
 
<script>
  // Load the JSON specification for Visualization 2
  vegaEmbed('#vis2', 'interactive_scatter.json').catch(console.error);
</script>
 
**Writeup:**

The scatter plot visualizes the relationship between building square footage and the year they were acquired, offering insights into trends over time and differences between agencies. The x-axis encodes the Year Acquired (quantitative), and the y-axis represents Square Footage (quantitative), with color used to distinguish buildings by Agency Name (nominal). The dataset was cleaned by removing rows with missing or non-numeric values in the Year Acquired and Square Footage columns. Interactivity is introduced with a legend filter, allowing users to select and highlight specific agencies, making it easier to compare data points by agency. This plot expands upon Homework #5 by adding interactivity and using Altair's enhanced features, which provide a more dynamic and informative user experience.
 
 
#### Resources
 
- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis](https://github.com/ekal2saloni/HW6_Jekyll/blob/main/Workbook.ipynb)
