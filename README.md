# Climate-Change-EDA
---

## Understanding Climate Change with Machine Learning Image source: 
![88926906-c9ed-45a4-8406-f401dbab7588 sized-1000x1000](https://user-images.githubusercontent.com/24231101/67533103-acaeea00-f67d-11e9-93c2-d498aad58907.jpg)

The Daily CardinalClimate change has been a serious topic this year, I am sure that if you live on planet earth you have heard that our planet is warming rapidly, and we need to act now so it's not too late. If you don't believe in climate change, don't worry that's why I am here, and hopefully, by the end of this reading, you will understand why this is so serious and will want to join the climate strike movement. 

Most of us have already heard about the Swedish climate activist Greta Thunberg, the 16-year-old activist who has inspired thousands of people to act on this matter - Greta, if you ever read this I would like to take a moment to say thank you for all your hard work and efforts, you are such an inspiration, and I stand with you. - Greta has been one of the main inspirations why I started this project. 
![GretaThunberghs2option1569656660539png](https://user-images.githubusercontent.com/24231101/67533159-db2cc500-f67d-11e9-92fd-ea3be48a60be.png)

During my Geology Science & Letter course at Make School, we have been discussing and learning different catastrophic events that have been happening in the world or in the surroundings of San Francisco Bay Area, and as part of the requirement of the course we have to pick one of the topics discussed in the classroom and do a slide deck that talks about the given topic, as strong-minded individual I asked myself, "Why not combine my skills as a Software Engineer & Data Scientist student with the course content?!", and my instructor Amy Young agreed with the idea, so here we are. 
![Enlight396 2](https://user-images.githubusercontent.com/24231101/67533277-3bbc0200-f67e-11e9-8856-ae1f550c16bd.JPG)

Throughout the past weekend, some of my peers and I formed a team called "WePlanet" and participated in the NASA Space Apps Challenge, where we won 1st place and were nominated for the Global Competition for developing an App called MiTerra, a gamified educational experience that teaches kids bout solutions to climate change and other possible catastrophes through interactive challenges. After participating in this hackathon, I started wondering how much CO2 there is in the atmosphere and how that has been affecting the temperature of our home planet, so I went to Berkley Earth which they have gathered and combined data from NASA's GISTEMP, UK's HadCrut, and I also included data from the NOAA's Mauna Loa Observatory to do this Exploratory Data Analysis (EDA). Before I show you my findings, I wanted to go over a few things first. 

#### What water issue will I be addressing on this EDA? 
As I mentioned above, this dataset will only be addressing CO2 in the atmosphere and temperature changes all over the world. Here is some content about the data: 

"The carbon dioxide record from Mauna Loa Observatory, known as the "Keeling Curve," is the world's longest unbroken record of atmospheric carbon dioxide concentrations. Scientists make atmospheric measurements in remote locations to sample air that is representative of a large volume of Earth's atmosphere and relatively free from local influences. This dataset includes a monthly observation of atmospheric carbon dioxide (or CO2) concentrations from the Mauna Loa Observatory (Hawaii) at a latitude of 19.5, the longitude of -155.6, and elevation of 3397 meters. 
Columns 1–3: Provide the date in the following redundant formats: year, month and decimal date Column 
4: Monthly CO2 concentrations in parts per million (ppm) measured on the 08A calibration scale and collected at 24:00 hours on the fifteenth of each month. 
Column 5: The fifth column provides the same data after a seasonal adjustment, which involves subtracting from the data a 4-harmonic fit with a linear gain factor to remove the seasonal cycle from carbon dioxide measurements 
Column 6: The sixth column provides the data with noise removed, generated from a stiff cubic spline function plus 4-harmonic functions with linear gain. 
Column 7: The seventh column is the same data with the seasonal cycle removed."

"The Berkeley Earth Surface Temperature Study combines 1.6 billion temperature reports from 16 pre-existing archives. It is nicely packaged and allows for slicing into interesting subsets (for example by country). They publish the source data and the code for the transformations they applied. They also use methods that allow weather observations from a shorter time series to be included, meaning fewer observations need to be thrown away. 
In this dataset, they have included several files: Global Land and Ocean-and-Land Temperatures: Date: starts in 1750 for average land temperature and 1850 for max and min land temperatures and global ocean and land temperatures LandAverageTemperature: global average land temperature in celsius LandAverageTemperatureUncertainty: the 95% confidence interval around the average LandMaxTemperature: global average maximum land temperature in celsius 

- LandMaxTemperatureUncertainty: the 95% confidence interval around the maximum land temperature 
- LandMinTemperature: global average minimum land temperature in celsius 
- LandMinTemperatureUncertainty: the 95% confidence interval around the minimum land temperature.
- LandAndOceanAverageTemperature: global average land and ocean temperature in celsius.
- LandAndOceanAverageTemperatureUncertainty: the 95% confidence interval around the global average land and ocean temperature Other files include: 
- Global Average Land Temperature by Country
- Global Average Land Temperature by State
- Global Land Temperatures By Major City
- Global Land Temperatures By City"

#### What generally causes this kind of issue? 
Earth's temperature depends on the balance between energy entering and leaving the planet's system. When incoming energy from the sun is absorbed by the Earth system, Earth warms. When the sun's energy is reflected back into space, Earth avoids warming. When absorbed energy is released back into space, Earth cools. Many factors, both natural and human, can cause changes in Earth's energy balance, including: Variations in the sun's energy reaching Earth Changes in the reflectivity of Earth's atmosphere and surface Changes in the greenhouse effect, which affects the amount of heat retained by Earth's atmosphere.

#### Why is this relevant and how Climate Change will affect me?

Earth's climate is changing faster than at any point in the history of modern civilization, primarily as a result of human activities. Climate changes have been affecting us already across every region in the world and in many different sectors that are extremely important to society such as human health, agriculture and food security, water supply, transportation, energy, ecosystems, and others - and are expected to become increasingly disruptive throughout the years. The Fourth National Climate Assessment (NCA4), developed by the U.S. Global Change Research Program (USGCRP), is a state-of-the-science synthesis of climate knowledge, impacts, and trends across U.S. regions and sectors to inform decision making and resilience-building activities across the country. It is the most comprehensive and authoritative assessment to date on the state of knowledge of current and future impacts of climate change on society in the United States.

What to read more? Here is the article [link](https://medium.com/@ElliotBriant/understanding-climate-change-with-machine-learning-fb45a047dd2b)
