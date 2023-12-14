Well done, you have completed all of the subjects of this course and arrived at the final challenge, the course project! This project is designed to assess your skills in the material covered in the course. So, this is your opportunity to apply what you have learned and work on a real-world dataset.

The dataset that you will be working with is collected from multiple public resources published by the Federal Statistical Office of Switzerland. It contains most of the demographic and geographic information for all communes in Switzerland.

More specifically, the dataset contains the following information for each commune in Switzerland:

The canton where the commune is located
Name of the commune
Language
Number of residents
Population density per km²
Percentage of residents aged from 0 to 19 years
Percentage of residents aged from 20 to 64 years
Percentage of residents aged 65 years and more
Number of private households
Surface area in km²
Percentage of the Settlement area
Percentage of the Agricultural area
Percentage of the Wooded area
Percentage of the Unproductive area
East coordinate of the center
North coordinate of the center
Median elevation in meters
You can download the dataset p1_communes.csv from the Resources tab.

Doing the project work
The project is made up of five tasks A to E, and the instructions for each of these you will find in the next unit. You need to complete all tasks, upload your notebook to your GitHub repository, and finally “submit” your project on the platform.

What should your Git repository look like?
When you submit your project, your GitHub repository should contain the following structure:

Repository/
├── p1_communes.csv
└── communes_solution.ipynb            
What should your notebook look like?
THE LAYOUT OF THE NOTEBOOK
You should use Markdown cells to create a section for each task and comment on your workflow throughout the project. This should include a brief explanation of your thoughts for each task as well as a detailed discussion of your approaches, observations, and decisions.

RESTART KERNEL & RUN ALL CODE CELLS
It must be possible for instructors to run your notebook from beginning to end without amending the code or generating any error messages. The quickest way to achieve this is to click on the “Kernel” tab in your notebook and select the “Restart Kernel & Run All” option, at the end of your project. Save and upload the executed, error-free notebook to your GitHub repository.

PLOTTING
All plots in your notebook should be self-explanatory, i.e., we should understand what is plotted without reading comments or code. Ensure that all of your plots have appropriate labels, title, and legend (if applicable). Also, ensure that the plots and fonts have proper sizes.

CODE OF CONDUCT AND PLAGIARISM
All content (e.g. code and comments) in your project submission is either (1) written by yourself or (2) where this is not the case, that you clearly highlight the extent of the copied content and provide a reference to its source. Not abiding by this rule is called plagiarism and can lead to penalties (see EPFL’s Directives and the consequences of committing plagiarism).

In the next unit, you are given a detailed list of tasks that you will need to accomplish to complete the project.

A. An overview of the dataset
The objective of this task is to gain some general information about the dataset before starting your exploration journey. By the end of this task, you will know about the number of observations, the index and columns, the data types, and the missing observations in the dataset. These are necessary information to know about any dataset before jumping into data exploration.

Import the data as a Pandas DataFrame and name it as df.
Check the number of rows and columns.
Display the first few entries of the DataFrame.
Obtain the index labels, and then show the column names as a list.
Check the data type for each column.
Check if there are any missing values and show the rows that contain the missing values.
If necessary remove any observations to ensure that there are no missing values and the values in each column are of the same data type.
B. Exploration: numerical summaries, indexing and grouping
Now that you are familiar with the general structure of the dataset, you can start an exploration adventure! Data exploration or explanatory data analysis enables you to tell a story with the data. It can be done in several ways depending on the objective and data types. In this task, you use your data summarization and aggregation skills to explore the data.

Obtain the mean, minimum and maximum value for each column containing numerical data. Your output should preferably show only the three requested statistics and not the full table of descriptive statistics.
List the 10 most populated communes, ordered by their number of residents.
List the 10 least populated communes, ordered by their number of residents.
Group the communes by canton and save them into separate .csv files, e.g. a ZH.csv with all the data for communes in Zurich (Do not include the .csv files in your submission).
Compute the population density at the canton level and rank the cantons from most dense to least dense. Clearly state and comment your observations.
Compute the number of communes in each canton where more than 50 percent of their populations are aged between 20 and 64 years old.
Compute the difference between the maximum and minimum elevations for each canton. Find the top 5 cantons that have the largest range of elevations?
C. Exploration: visualizations
Let’s continue the explanatory data analysis but this time with visualizations. Visual exploration is a powerful way to learn about the distributions and the relationship between columns and add them to your story. In this task, you use your data visualization skills to explore the data.

Your task is to obtain a horizontal bar plot that shows the top 10 populated communes. Your bar chart should have the names of the communes listed vertically along the 
y
-axis and the 
x
-axis should show the populations. Ensure that the chart has an appropriate title and labels.

For the top 10 populated communes of the previous step, your task now is to plot a horizontal stacked bar chart that shows how their lands are divided into the 4 area types: Settlement, Agricultural, Wooded, Unproductive. Remember that these 4 area types represent the percentages and should add up to 100 for each commune. Ensure that the chart has an appropriate title, legend and labels. Analyze the plot and clearly state and comment your observations. Your output should look like the following plot.


We are interested in the number of communes and their proportions of young residents (0-19yrs). Your task is to obtain a histogram that shows the number of communes for which this proportion falls into the following intervals:

5%-10%
10%-15%
15%-20%
20%-25%
25%-30%
30%-35%
Ensure that the chart has an appropriate title and labels, and has width of 5 and height of 4. Hint: you can use the figsize to adjust the size. And you can specify the boundaries of the intervals by feeding a list to the bins parameter in the hist-method.

Your task is to investigate the distributions of the age group 0-19 years, which is a numerical variable, across four language regions, which is a categorical variable. Analyze the plot and clearly state and comment your observations. Hint: you can choose from Seaborn one of the violin plot, box plot or boxen plot for this purpose.

Your task is to do the previous task for the three age groups 0-19 years, 20-64 years, and 65 years or over. In order to make the comparison easy, you should make a plot with one subplot per age group (plot with 1 row and 3 columns). Ensure that the subplots have appropriate titles, legends, and labels. Also, ensure that they have proper sizes and there is enough space between them.

The 
y
-axis of the subplot should show the percentages of the populations for age groups, ranging from 0 to 80%. Hint: you can use sharey parameter of the subplot.
Optional: add the observations into your subplot to see how they form the distributions. For instance, if you chose the box plot, you can draw a strip plot on the same axis as a complement to the box plot.

Your task is to use the pairplot from Seaborn and produce 3 plots to visually investigate the relation between the Agricultural area of communes and their Settlement area, Wooded area and the Unproductive area.

Are the relations linear?
Use the Elevation as the color-code variable in the plot and show that communes that are located in high altitudes have very low Settlement and Agricultural areas, but have a lot of Unproductive areas.

Your task is to draw a map of Switzerland using the East and North coordinates of communes. Ensure that the plot has an appropriate title, legend and labels. Hint: you can use the Seaborn scatter plot for this task.

Use the Elevation as the color-code variable in the plot so that the you can see the three geographic regions, namely the Swiss Alps, the Central Plateau and the Jura. Your output should look like the following plot.
Re-do the same plot but this time with the Language as the color-code variable.
Analyze both plots and clearly state and comment your observations in each case.

Your task is to obtain the two plots from the previous task as subplots (with 1 row and 2 columns). Ensure that the plots have appropriate titles, legends and labels. Also, ensure that they have proper sizes and there is enough space between them.
D. Probabilities
The objective of this task is to assess your understanding of the conditional probability, but it could be also considered as a data exploration question.

Compute the probability that a randomly selected commune with elevation over 2000 is from the canton of Valais.

E. Matrices
The objective of this task is to assess some of the skills you have learned in this course, but later on you will see that it becomes an important preprocessing step before using Machine Learning models.

Define a data frame matrix whose rows correspond to communes and the columns to the cantons. Fill in the matrix with 0/1 values where entry 
(
i
,
j
)
 is a 1 if the commune in row 
i
 is in the canton in column 
j
 and a 0 otherwise.
