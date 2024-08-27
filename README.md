
# Sales Report: Videogames  

This dashboard helps us to understand how video games's sales have been changing over time and depending on the Region, Platform and  year as some examples.

In this example we have the amount of 11.359 unique games from 1980 to 2017 classified by Year, Category, Editorial and amount of money received (millions). Every game was sold all over the world and here we can compare between 4 Regions (North America, Europe, Japan and Others)

As we can see, almost 50% of the sales were in North America (49,15%) if we don't filter anything, Action category was the preferred one with 1900 different games and the Platform which generated more amount of money was "X360". Finally, we can say that the best year (economically talking) was 2008 with 351,44 millions generated.
Studying trends can be very useful to understad the past but also the present and to try to predict the future and this kind of charts are perfect for this task.

## Steps

1. Obtain data from a New Source > Excel file > Transform data before Load
2. Evaluate the Quality of the columns, Distribution and the Profile to understad the data as a preview.
3. Check the data type of every column because Power BI can miss sometimes with the automatic detection.
4. Select the colums "NA sales", "EU sales", "Others sales" and "JP sales" > Unpivot colums so we can create an "Attibute column" which allow us to filter by Region (similar values in the same colomn, in this case we have Regions).
5. If we are sure we Load the data
6. We only have a fact table so we dont need to do anything with the Model Structure.

### DAX
In this example i only created a measure called "Unique Games"

Unique Games = DISTINCTCOUNT ('Video Games sales [Name]') 

This measure reveals the number of different values in a column, in this example the column "Name"

### Storytelling

1. We have 6 slicers that allow us to filter the information as we are interested in. Filtering one of them produce an automatic change in the rest of slicers.
2. I placed a "Delete filters" button which let us delete every selection we have done before in every slicer
3. In this example i created 3 bar charts. "Sold by Category and Region","Sold by Platform and Region" and "Sold by Year and Region". Every one ofthem have the same Leyend -> Region.
4. A donut chart to understand the Sales by Region with porcentages
5. A table that explains the "Sales details" with 5 colums. 
5.1. I configured a conditional formatting for the column "Sold (millions)"
Field components > choose the column "Sold (millions) > activate background > formatting style > Gradient > Apply to values > Lowest value with a color and highest value with another.
The conditional formatting is really useful because we can see really fast the better games economically talking (or the worst)
