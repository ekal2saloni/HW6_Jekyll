# Building Inventory Dataset Visualisations
*Submitted By Saloni Ekal (ekal2@illinois.edu)*
 
 
## Visualization 1: Exploring Average Square Footage by Building Usage: Filtered by Agency (Interactive)
<div id="vis1"></div>
 
<script src="https://cdn.jsdelivr.net/npm/vega@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-lite@5"></script>
<script src="https://cdn.jsdelivr.net/npm/vega-embed@6"></script>
 
<script>
  // Load the JSON specification for Visualization 1
  vegaEmbed('#vis1', 'interactive_bar_chart.json').catch(console.error);
</script>
 
**Writeup:**

This bar chart visualizes the average square footage of buildings based on their usage description, with an option to filter by specific agencies. Each bar represents a usage type, making it easy to compare how different categories stack up in terms of average square footage. The interactivity comes from a drop-down menu that lets you focus on a particular agency, simplifying the view to suit your exploration. Additionally, hovering over a bar reveals a tooltip with details like the agency name, usage description, and average square footage, which adds depth to the visualization.

The chart uses the x-axis to encode the average square footage (a quantitative variable) and the y-axis to represent the usage description (a nominal variable). Colors are mapped to the usage descriptions to differentiate the bars, though no legend is needed since the y-axis already provides the category names. Before creating this chart, the data was transformed by grouping it by agency name and usage description, then calculating the mean square footage for each group. This step was essential to simplify the dataset and focus on averages instead of individual buildings. This approach ties back to Homework #5, where filtering and aggregation were also used to streamline data for better visual clarity.
 
 
## Visualization 2 : Year of Acquisition vs. Square Footage: An Agency-Level Analysis (Interactive)
<div id="vis2"></div>
 
<script>
  // Load the JSON specification for Visualization 2
  vegaEmbed('#vis2', 'interactive_scatter_plot.json').catch(console.error);
</script>
 
**Writeup:**

The scatter plot explores the relationship between the year a building was acquired and its square footage, with color-coded points representing different agencies. Each dot is a building, and users can interact in two ways: they can highlight specific points by clicking on them or filter the view by selecting multiple agencies in the legend. Tooltips provide additional context by showing details like the building's name, square footage, and acquisition year, making it easier to spot interesting patterns or outliers.

In this visualization, the x-axis represents the year acquired (a quantitative variable), and the y-axis captures the square footage (also quantitative). The colors are mapped to agency names, with a distinct palette ensuring that points for different agencies are easy to distinguish. Interactivity is enhanced through opacity changes—highlighted points remain fully visible, while the rest fade slightly to provide context without overwhelming the view. Unlike the bar chart, this scatter plot works directly with the raw data instead of pre-aggregated values, offering a closer look at individual buildings. This builds on techniques used in Homework #5, where interactivity also played a key role in exploring subcategories and uncovering trends.
 
 
#### Resources
 
- [The Data](https://raw.githubusercontent.com/UIUC-iSchool-DataViz/is445_data/main/building_inventory.csv)
- [The Analysis](https://github.com/ekal2saloni/HW6_Jekyll/blob/main/Workbook.ipynb)
