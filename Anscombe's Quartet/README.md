# Anscombe's Quartet

For more information about this example, see:

- <https://en.wikipedia.org/wiki/Anscombe%27s_quartet>
- <https://eagereyes.org/criticism/anscombes-quartet>

You can download the [`demo.twbx`](demo.twbx) file for the full Tableau Desktop workbook demonstrated in class. However, I recommend you try to recreate the visualizations from scratch using the steps below.

## Getting Started

:octocat: [Download Data](data/anscombe.csv)

1. Under the "Data" menu, select "Connect" » "To a File" » "Text File" and then open `anscombe.csv` from the dialog window.

2. You should see an "X", "Y", "Group" and "#" column once the data is loaded. Click "New Worksheet" near the left bottom of the screen to get started.

## Simple Table

<a href="img/table.png"><img src="https://usf-cs360-2017.github.io/lectures/Anscombe%27s%20Quartet/img/table.png" height="250"></a><br/>
:cinema: [Walkthrough Video](https://youtu.be/tohwAzdmpP8)

1. Under the "Dimensions" panel, drag "Group" and "Measure Names" to the "Columns" panel. Make sure "Group" appears *before* "Measure Names".

2. Under the "Measures" panel, drag "#" to the "Rows" panel. Select the dropdown for "SUM(#)" and select "Dimension". Under the same dropdown, select "Discrete".

3. Under the "Measures" panel, drag "Measure Values" to the "Text" box in the "Marks" panel.

4. Under the "Measure Values" panel, drag "SUM(#)" and "SUM(Number of Records)" off to remove them.

5. Under the "Measure Values" panel, change both the "SUM(X)" and "SUM(Y)" to "Attribute" in the dropdown menu.

6. *Optional:* Under the "Measures" panel, drag "Measure Values" onto the "Color" box in the "Marks" panel. Click the "Color" box and then the "Edit Colors" button. In the dialog window that opens, select "Red-Blue Diverging" from the "Palette" dropdown box. Click the "Advanced" button and change the "Start" and "End" values to 0 and 20 respectively. Click the "Apply" and "OK" buttons.

## Simple Statistics

Using a similar approach as above, see if you can re-create the following simple statistics table:

<a href="img/stats.png"><img src="https://usf-cs360-2017.github.io/lectures/Anscombe%27s%20Quartet/img/stats.png" height="250"></a>

You do not have to re-create the look and feel exactly (i.e. you do not have to modify the panel placement, titles, font, etc. to match the screenshot above exactly.

## Simple Scatterplot

<a href="img/scatter.png"><img src="https://usf-cs360-2017.github.io/lectures/Anscombe%27s%20Quartet/img/scatter.png" height="250"></a>

0. Create a new worksheet.

1. Under the "Measures" panel, drag "X" to the "Columns" panel and "Y" to the "Rows" panel. Change both to "Dimension" using the dropdown.

2. Under the "Dimensions" panel, drag "Group" to the "Color" box of the "Marks" panel. Select "Circle" as the mark.

3. Right-click the "X" label and select "Edit Axis" from the menu. Change the "Range" radio button to "Fixed" and set the start and end to "0" and "20" respectively. Click the "Tick Marks" button and select the "Fixed" radio button for "Major tick marks". In the "Every" box, enter "5" to show a tick mark every 5 units. Click the "Apply" and "OK" buttons when done. Repeat this process for the "Y" axis.

4. Change the "X" or "Y" width or height so that the boxes formed by the tick lines are roughly square, giving us a nice 1:1 aspect ratio.

5. Right-click the plot area and select "Trend Lines" and "Show Trend Lines" from the menu.

6. Right-click the plot area and select "Trend Lines" and "Edit Trend Lines" from the menu. Unselect "Show Confidence Bands" from the dialog box.

7. *Optional:* Under the "Dimensions" panel, drag "Group" to the "Columns" panel *before* the "X" dimension. This will give you the small multiples view.

<a href="img/multiples.png"><img src="https://usf-cs360-2017.github.io/lectures/Anscombe%27s%20Quartet/img/multiples.png" height="250"></a>
