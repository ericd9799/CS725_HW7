# Exploratory Analysis Process
Starting with the datasets and proposed questions from [Homework 5](https://git-community.cs.odu.edu/ediep/CS725-HW5), I had to explore the dataset for each question to see which dataset and question was feasible to continue exploring.

The initial question is, how has the access to drinking water and sanitation changed over time for rural areas?

The dataset I am using for analysis is provided by World Health Organization. The dataset used are [basic and safely managed sanitation services data](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en), and [basic and safely managed drinking water services data](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en).

For the dataset, CSV files were provided and they were not formatted -- no borders, duplicate header columns. Thus, I had to format the files to allow for it to be easier to explore. Within the dataset, there are columns rating the country's access to basic services and managed services for both sanitation and drinking water services. Managed sanitation service is improved sanitation facility where excreta are safely disposed of in situ or treated off site. While basic sanitation service is improved sanitation facilities that are not shared with other households. Managed drinking water service is where drinking water is accessible on premises and free from faecal and chemal contamination. Basic drinking water service is where drinking water from an improved source where the population does not have to travel more than 30 minutes round-trip.

Since I am only interested in the ratings for rural areas, I removed columns from the dataset that were not not of interest. The dataset had blank values, I assumed they were zero and populated them with "0".

Below chart is the initial chart created for one country to see how the chart would look like.
![alt text](Initial_Chart.PNG "Initial Chart")

Looking at the initial chart and the dataset, it would not be feasible to plot the basic and managed drinking-water services ratings for 194 countries. Thus, I limited to only countries where they had both basic managed drinking-water services rating populated. Below is the chart produced.
![alt text](All_Fields_Populated.PNG "Basic and Managed Drinking-Water Services Populated")

# References
 * [CS725, Spring 2018 - Homework 5](https://git-community.cs.odu.edu/ediep/CS725-HW5)
 * [WHO/UNICEF Join Monitoring Programme for Water Supply, Sanitation, and Hygiene](https://washdata.org/data)
 * [Basic and safely managed sanitation services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHSANITATION?lang=en)
 * [Basic and safely managed drinking water services Data by country by World Health Organization](http://apps.who.int/gho/data/node.main.WSHWATER?lang=en)