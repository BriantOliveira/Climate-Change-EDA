# Climate-Change-EDA
---

Understanding Climate Change with Machine Learning
Image source: The Daily CardinalClimate change has been a serious topic this year, I am sure that if you live on planet earth you have heard that our planet is warming rapidly, and we need to act now so it's not too late. If you don't believe in climate change, don't worry that's why I am here, and hopefully, by the end of this reading, you will understand why this is so serious and will want to join the climate strike movement.
Most of us have already heard about the Swedish climate activist Greta Thunberg, the 16-year-old activist who has inspired thousands of people to act on this matter - Greta, if you ever read this I would like to take a moment to say thank you for all your hard work and efforts, you are such an inspiration, and I stand with you. - Greta has been one of the main inspirations why I started this project.
During my Geology Science & Letter course at Make School, we have been discussing and learning different catastrophic events that have been happening in the world or in the surroundings of San Francisco Bay Area, and as part of the requirement of the course we have to pick one of the topics discussed in the classroom and do a slide deck that talks about the given topic, as strong-minded individual I asked myself, "Why not combine my skills as a Software Engineer & Data Scientist student with the course content?!", and my instructor Amy Young agreed with the idea, so here we are.
WePlanet TeamThroughout the past weekend, some of my peers and I formed a team called "WePlanet" and participated in the NASA Space Apps Challenge, where we won 1st place and were nominated for the Global Competition for developing an App called MiTerra, a gamified educational experience that teaches kids bout solutions to climate change and other possible catastrophes through interactive challenges.
After participating in this hackathon, I started wondering how much CO2 there is in the atmosphere and how that has been affecting the temperature of our home planet, so I went to Berkley Earth which they have gathered and combined data from NASA's GISTEMP, UK's HadCrut, and I also included data from the NOAA's Mauna Loa Observatory to do this Exploratory Data Analysis (EDA). Before I show you my findings, I wanted to go over a few things first.
What water issue will I be addressing on this EDA?
As I mentioned above, this dataset will only be addressing CO2 in the atmosphere and temperature changes all over the world. Here is some content about the data:
The carbon dioxide record from Mauna Loa Observatory, known as the "Keeling Curve," is the world's longest unbroken record of atmospheric carbon dioxide concentrations. Scientists make atmospheric measurements in remote locations to sample air that is representative of a large volume of Earth's atmosphere and relatively free from local influences.
This dataset includes a monthly observation of atmospheric carbon dioxide (or CO2) concentrations from the Mauna Loa Observatory (Hawaii) at a latitude of 19.5, the longitude of -155.6, and elevation of 3397 meters.
Columns 1–3: Provide the date in the following redundant formats: year, month and decimal date
Column 4: Monthly CO2 concentrations in parts per million (ppm) measured on the 08A calibration scale and collected at 24:00 hours on the fifteenth of each month.
Column 5: The fifth column provides the same data after a seasonal adjustment, which involves subtracting from the data a 4-harmonic fit with a linear gain factor to remove the seasonal cycle from carbon dioxide measurements
Column 6: The sixth column provides the data with noise removed, generated from a stiff cubic spline function plus 4-harmonic functions with linear gain
Column 7: The seventh column is the same data with the seasonal cycle removed.
The Berkeley Earth Surface Temperature Study combines 1.6 billion temperature reports from 16 pre-existing archives. It is nicely packaged and allows for slicing into interesting subsets (for example by country). They publish the source data and the code for the transformations they applied. They also use methods that allow weather observations from a shorter time series to be included, meaning fewer observations need to be thrown away. In this dataset, they have included several files:
Global Land and Ocean-and-Land Temperatures:
Date: starts in 1750 for average land temperature and 1850 for max and min land temperatures and global ocean and land temperatures
LandAverageTemperature: global average land temperature in celsius
LandAverageTemperatureUncertainty: the 95% confidence interval around the average
LandMaxTemperature: global average maximum land temperature in celsius
LandMaxTemperatureUncertainty: the 95% confidence interval around the maximum land temperature
LandMinTemperature: global average minimum land temperature in celsius
LandMinTemperatureUncertainty: the 95% confidence interval around the minimum land temperature
LandAndOceanAverageTemperature: global average land and ocean temperature in celsius
LandAndOceanAverageTemperatureUncertainty: the 95% confidence interval around the global average land and ocean temperature
Other files include:
Global Average Land Temperature by Country

Global Average Land Temperature by State

Global Land Temperatures By Major City

Global Land Temperatures By City

What generally causes this kind of issue?
Earth's temperature depends on the balance between energy entering and leaving the planet's system. When incoming energy from the sun is absorbed by the Earth system, Earth warms. When the sun's energy is reflected back into space, Earth avoids warming. When absorbed energy is released back into space, Earth cools. Many factors, both natural and human, can cause changes in Earth's energy balance, including:
Variations in the sun's energy reaching Earth
Changes in the reflectivity of Earth's atmosphere and surface
Changes in the greenhouse effect, which affects the amount of heat retained by Earth's atmosphere
Why is this relevant and how Climate Change will affect me?
Earth's climate is changing faster than at any point in the history of modern civilization, primarily as a result of human activities. Climate changes have been affecting us already across every region in the world and in many different sectors that are extremely important to society such as human health, agriculture and food security, water supply, transportation, energy, ecosystems, and others - and are expected to become increasingly disruptive throughout the years.
The Fourth National Climate Assessment (NCA4), developed by the U.S. Global Change Research Program (USGCRP), is a state-of-the-science synthesis of climate knowledge, impacts, and trends across U.S. regions and sectors to inform decision making and resilience-building activities across the country. It is the most comprehensive and authoritative assessment to date on the state of knowledge of current and future impacts of climate change on society in the United States.


---

Since we've covered some of the essentials things about climate change, we can move on to what I have discovered throughout my Exploratory Data Analysis.
As I was importing the data and analyzing some of the columns and rows in the dataset, I notice that there were some missing data - A few of the rows had empty values (NaN). One of the major differences between data found in tutorials and data in the real world is that real-world data is rarely clean and homogeneous. Many interesting datasets will have some amount of data missing. To make matters even more complicated, a lot of different data sources may indicate missing data in different ways - so it was important to remove these values from the dataset because they could lead to wrong predictions or classification in our model.
Now that the dataset is clean, I was able to move forward with my analysis. One of the immediate things I noticed was that I needed to modify the dates listed, the dataset had listed Year-Month-Day and for my first prediction, I only needed the year.
For my first prediction, I selected only the average temperature of every state in the United States. The first plot that I decided to do in order to understand the data that we are working with was a scatter plot. I wanted to visualize the average temperature of the states in the US that were above and below 9° degrees.
A scatter plot is a graph in which the values of two variables are plotted along two axes, the pattern of the resulting points revealing any correlation present.
My next thought process was to create a new dataframe which would contain the average Carbon Dioxide in the atmosphere per year, and then do a Linear Relationship to visually see how much it has changed over the years. For this plot, I utilized a python library called seaborn.
Two main functions in seaborn are used to visualize a linear relationship as determined through regression. These functions, regplot() and lmplot() are closely related and share much of their core functionality. It is important to understand the ways they differ, however, so that you can quickly choose the correct tool for a particular job.
In the simplest invocation, both functions draw a scatterplot of two variables, x, and y, and then fit the regression model y ~ x and plot the resulting regression line and a 95% confidence interval for that regression.
This plot shows the increase in Carbon Dioxide in the atmosphere over the years. Unfortunately, during the 1760s which was when the 1st industrial revolution started our technology wasn't advanced enough, and it wasn't until 10 years after the 3rd industrial revolution that our technology has advanced so we could keep track of Carbon Dioxide in the atmosphere.
As you can see in the plot above, in 2010 we have reached almost 400 parts-per-million (ppm) of Carbon Dioxide globally. After discovering this result, I wanted to check if there were any correlation.
Correlation is a statistical measure that indicates the extent to which two or more variables fluctuate together. A positive correlation indicates the extent to which those variables increase or decrease in parallel; a negative correlation indicates the extent to which one variable increases as the other decreases.
Now that we have discovered a few important information, I was tempted to visualize the average levels of CO₂ in the atmosphere per month. For this visualization, I used a python library called plotly, this library allows your plots to be interactive.
This plot revealed that in 2017 the average level of CO₂ was 406.07 (ppm), which is a major swing compared to the level of CO₂ in 2010. Now let's check what does the Seasonal fluctuations of CO₂ levels are.
As I mentioned before, all of these data visualizations done with plotly are interactive, so if you want to go on the notebook and interact with the plot and see the numbers for yourself, I will leave the link to the source code available.
All of these results are very interesting and super insightful, my next step was to train model to able to create more data-driven insights, after training the model I was able to create a prediction and visualize the actual levels of CO₂ and compare it with the predicted levels, and the results were shocking.
As you can see in the plot above, I made sure to mark the year 2030. If you are not aware 2030, was the year that the IPCC reported to the United Nations, that if we don't act and change our habits to reduce the levels of CO₂ in the atmosphere the damages will be irreversible. As you can see in January 2030 the predicted level of CO₂ in the atmosphere will be 437.3 (ppm). This is a massive change!
Now let's take a look in the state and country that had the highest average temperature level in the dataset, and what year was that temperature was recorded.
Bill Nye Explains Carbon Pricing and Climate Change videoIf by now you haven't realized that climate change is a real issue and it affects our entire planet, you should read this article again, and again, until you realize that we have to act now! There isn't a plan B! Earth is our home planet and we have to take care of it.
How can I contribute to solve this problem?
Unite for bold climate action
Use energy wisely - and save money too!
Get charged up with renewables
Eat for a climate-stable planet
Start a climate conversation
Green your commute
Consume less, waste less, enjoy life more
Invest in renewables and divest from fossil fuels
Support or join youth-led movements
Get politically active and vote

If you made it this far, thank you for reading this article. If you want to find out more about what you can do or study the topic more I'll leave a few links to some useful resources. Also, if you want to contribute to this notebook and create more data-driven insights I'll also link the repository where this code will be available, feel free to fork it and star the project on Github.
United we can make a change & united we can be the change!
