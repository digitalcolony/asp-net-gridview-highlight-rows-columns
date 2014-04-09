asp-net-gridview-highlight-rows-columns
=======================================

Adding row and column highlight to a Gridview

This code is inspired by Ryan Scherf’s Table Row and Column Highlighting. It’s a slick solution to helping users read tabular data. I thought it would be nice to add that functionality to the ASP.NET. So I created a single function that would add Ryan’s column and row highlighting code to our GridView control.

http://ryanscherf.net/demos/crosshairs/

Files Needed

On Ryan’s demo site, you can find the crosshair javascript file (aka CSS/JavaScript Table Hilighting). You will also need a crosshair CSS file. 

Crosshair.css

Place this file either in your App_Theme folder (if you are using themes), embed it in the head of the document or link to it externally.

AddCrossHairToGridView

After loading your GridView, make a call to the AddCrossHairToGridView function. It takes 5 parameters.

gv: The ID of the GridView Control you wish to add highlighting to.
top: How many rows from the top should not have highlighting.
right: How many rows from the right should not have highlighting.
bottom: How many rows from the bottom should not have highlighting.
left: How many rows from the left should not have highlighting.

I dropped the Javascript file inside the same folder in this example. Update the path in the RegisterClientScriptInclude line to point to whatever location you use.
