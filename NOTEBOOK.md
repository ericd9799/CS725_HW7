# Exploratory Analysis Process
Starting with the datasets and proposed questions from [Homework 5](https://git-community.cs.odu.edu/ediep/CS725-HW5), the question selected to explore is, how has the access to drinking water and sanitation changed over time for rural areas? The datasets, [basic and safely managed sanitation services data](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en) and [basic and safely managed drinking water services data](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en), used for analysis are provided by the World Health Organization.

The datasets were provided as CSV files. The datasets contain a list of alphabetically order countries. For each country, there are columns populated with what percentage of the population is using either basic or managed services for drinking-water and sanitation. These percentage values are further split between rural and urban areas. To understand the difference between basic and managed services, I looked up the defintion of each.

Basic drinking water service is defined as drinking water is from an improved source where the population does not have to travel more than 30 minutes round-trip. Managed drinking water service is defined as drinking water is accessible on premises and free from fecal and chemical contamination. Basic sanitation service is defined as improved sanitation facilities that are not shared with other households. Managed sanitation service is defined as improved sanitation facility where excreta are safely disposed of in situ or treated off site. 

Since both dataset files are identical, after I figure out what transformation is needed for one, I will replicate for the other. Since I am only interested in the ratings for rural areas, I removed columns from the dataset which pertained to urban area. The dataset had blank values, I assumed they were zero and populated them with a zero.

Below chart is the initial chart created for a few countries. In the chart, there are two points for each year because it is connecting the percentage value between basic drinking-water services and managed drinking-water services. The line goes up and down because these countries did not have values for what percentage of the population has access to managed drinking-water services. This caused the graph to be illegible and unmeaningful.
![alt text](Pre_Initial_Chart.PNG "Initial Chart")

 I decided to filter out countries that did not have a value for basic drinking-water services and managed drinking-water services. Below is the chart produced.
![alt text](All_Fields_Populated.PNG "Basic and Managed Drinking-Water Services Populated")

The chart plotted the points incorrectly by connecting both basic and managed ratings as see in the initial chart. Again, there are two points for each year. Looking at both charts and the dataset, it would not be feasible to plot the basic and managed drinking-water services ratings for 194 countries for 15 years. I decided to narrow the question, how has the access to basic drinking-water and sanitation changed over time for rural areas? 

After narrowing the question, columns that did not pertain to basic drinking-water service were removed. With the question narrowed, I created a chart that displays the population with access to basic drinking-water in rural areas. Below is the produced chart.
![alt text](Initial_Chart.PNG "Population with Access to Basic Drinking-Water in Rural Areas")

From the chart, I explored the dataset and noticed there were countries where the rating was either 0%, or between 90% to 100% for rural areas having access to basic drinking for all years. I decided to filter out these countries, and the number of remaining countries is over 100. This would still cause the produced chart to be illegible if the data for drinking-water and sanitation are plotted for 100+ countries.

I added a new column to the dataset which contains the continent the country is located in. Adding this column will help further filter the data. I explored the data by filtering on the new column, and decided to narrow the data for analysis to countries within South America. The question changed to, how has the access to basic drinking-water and santitation changed over time in rural areas for countries in South America?

The graph below represents percentage of population for rural areas in South American countries with access to basic drinking-water service.
![alt text](Basic_Drinking_Water_SouthAmerica.PNG "Basic Drinking-Water Service for South American Countries")

The graph below represents percentage of population for rural areas in South America countries with access to basic sanitation service.
![alt text](Basic_Sanitation_SouthAmerica.PNG "Basic Sanitation Service for South American Countries")

I combined the datasets of both charts aboved to be able to compare the access to basic drinking-water services versus sanitation. By combining the data, the question changed to, how does access to basic drinking-water services compare to basic sanitation services in rural areas of South American countries? If all the points for each country were plotted on a single graph, it would cause the graph to be illegible. Thus, I decided to generate a graph for each country. With a graph generated for each country, the trend for basic drinking-water services and basic sanitation can be compared. To be able to compare between countries, small multiples was used to be able to display all the graph at once.
![alt text](SmallMultiple.png "Access to Basic Drinking-Water Service vs. Access to Basic Sanitation")

# References
 * [CS725, Spring 2018 - Homework 5](https://git-community.cs.odu.edu/ediep/CS725-HW5)
 * [Basic and safely managed sanitation services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en)
 * [Basic and safely managed drinking water services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en)
 * [Definition of Population Using At Least Basic Sanitation Services](http://apps.who.int/gho/data/node.wrapper.imr?x-id=4821)
 * [Definition of Population Using At Safely Managed Sanitation Services](http://apps.who.int/gho/data/node.wrapper.imr?x-id=4820)
 * [Definition of Population Using At Least Basic Drinking-Water Services](http://apps.who.int/gho/data/node.wrapper.imr?x-id=4818)
 * [Definition of Population Using Safely Managed Drinking-Water Services](http://apps.who.int/gho/data/node.wrapper.imr?x-id=4819)