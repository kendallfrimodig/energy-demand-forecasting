# Energy Forecasting for the Texas Power grid

**2/11/2022**

---

<p style="line-height:2">


Today I'm going to walk though a team project I recently participated in, focusing on energy demand forecasting. Texas was the subject matter, as it operates as
an independent energy grid (other states of US connected) and recently experienced a near meltdown in its basic generating capacity, as a result of the
winter storm of Valentines day 2021. Though the event was unprecedented, neighboring states fared the storm without the loss of life seen in Texas.
Me and my teammates thought a review of their preparedness tools might present an opportunity for positive change.


</p><br>





---
### Scope

<p style="line-height:2">


Energy must be produced in real time, to match demand - otherwise load shedding is necessary (temporary or prolonged blackouts) and as you might guess
one person does not have the authority to flip the switch for select plants in such a time sensitive situation. If the demand is not sufficiently
decreased in timed, the web of power-plants will collectively fall between This is a tricky line to walk  since coal or natural gas power plants aren't acquiring their resources
on-site


</p><br>





---
### Relevance

Before I get into some of the reasons an updated forecasting tool might better prepare Texas for another emergency, its worth highlighting that this was
on for the books,

![The 7 day average departure for the February](https://pbs.twimg.com/media/Eu2IqLqXYAMbkkb?format=jpg&name=large)



---
### Energy Prices


Accurate predictions of overall energy demand with respect to a states generation ceiling are crucial, and the rate of change (delta) of demand play a
significant role in price. Although your average Texan will pay a agreed upon rate, for protection against such price gouging, many are offered access to
market electricity pricing and indeed sign up. If you have 2 electric cars at home, utilizing the lower cost at night could save you alot of cash.  


![average price for electricity in Texas, Feb. 2021](https://www.eia.gov/todayinenergy/images/2022.01.07/main.svg)

To our knowledge, the energy information administration (EIA) is the provider of energy demand forecasts for individual providers.











# energy-demand-forecasting
Team project aimed to create a energy demand forecasting model which reacts to anomolies

Sources Cited: <br>
Cascading risks: Understanding the 2021 winter blackout in Texas [source 01](https://www.sciencedirect.com/science/article/pii/S22146296210019)<br>

Texas winter storm final death toll 246 [source 02](https://www.texastribune.org/2022/01/02/texas-winter-storm-final-death-toll-246/) <br>

The US has more power outages than any other developed country. Here’s why. [source 03](https://www.popsci.com/story/environment/why-us-lose-power-storms/) <br>

EIA energy explained: use of electricity [source 04](https://www.eia.gov/energyexplained/electricity/use-of-electricity.php#:~:text=Electricity%20consumption%20in%20the%20United,important%20to%20the%20U.S.%20economy.) <br>

EIA energy explained: electricity in the US [source 05](https://www.eia.gov/energyexplained/electricity/electricity-in-the-us.php) <br>




### BACKGROUND
The impact of Winter Storm Uri on the Texas power grid during February 2021 was catastrophic and a reminder of the growing degradation of the US electric grid. Persistent freezing temperatures caused wind turbines, nuclear power plants, and natural gas plants (which were already suffering from fuel shortages) to go offline, thereby decreasing the supply of electricity to a populace who was simultaneously increasing demand to stay warm and survive the storm. As the supply couldn’t keep up with the demand throughout the storm, the Electric Reliability Council of Texas (ERCOT) ordered rolling blackouts in order to avoid a complete collapse of the Texas power grid. ([source 01] (https://www.sciencedirect.com/science/article/pii/S22146296210019)). Around 10 million people were affected, 246 people died, and $130 billion in damages were attributed to the storm. ([source 01] (https://www.sciencedirect.com/science/article/pii/S22146296210019)). ([source 02] (https://www.texastribune.org/2022/01/02/texas-winter-storm-final-death-toll-246/)). These occurrences will become increasingly common as climate change exacerbates weather conditions and the weather grid continues to deteriorate. The US has more power outages than any developed country in the world due to aging facilities and deferred maintenance. The current status of the grid is untenable and will continue to impact the health and safety of all citizens. ([source 03](https://www.popsci.com/story/environment/why-us-lose-power-storms/)).
<br>
In 2020, the US consumed more than 3.8 billion MW hours of electricity with about 39% going to supply the residential sector (most of this being heating and cooling). These energy sources come from fossil fuels, such as natural gas, coal, and oil, and from renewables including, nuclear, wind, hydropower, solar, geothermal, and biomass. From a national perspective, the most used sources are natural gas, nuclear, and coal, but renewables are slowly becoming more predominant as technology improves and when the weather conditions are right. ([source 04] (https://www.eia.gov/energyexplained/electricity/use-of-electricity.php#:~:text=Electricity%20consumption%20in%20the%20United,important%20to%20the%20U.S.%20economy.)). ([source 05] (https://www.eia.gov/energyexplained/electricity/electricity-in-the-us.php)). The energy that reaches your home is from a variety of different sources and power plants that are most often located in your state or balancing authority region. Energy is lost to heat the further away it travels from the source, therefore keeping electricity use close to it’s generation will prevent energy loss when being transported over greater distance. As this is the case, it is imperative for each balancing authority to reliably predict demand and be able to match it within each region with net power generation.







### CONCLUSIONS AND FURTHER RESEARCH
As events like the 2021 Texas power crisis become more common with climate change and aging US energy grid infrastructure, it becomes increasingly important for the public to understand where their power comes from and how overall energy demand may affect them. In our exploratory data visualizations we show patterns of renewable power generation that can be useful for individuals who are interested in timing their use to minimize their carbon footprint. For example, individuals can use this type of demand forecast to time their power usage to lower cost times, such as for electric vehicle charging. Providing accurate energy demand forecasts are also important for energy grid operators. We developed a simple set of 1 hour forecast models that have the advantage of being fast and scalable (as opposed to ARIMA forecasts and others). Our triple smoothed exponential models are a good choice for streaming forecasts online. In addition, these types of models are not as influenced by long-past exogenous events such as previous-annual holidays. This allows them to follow recent patterns better.

Our next goal is to create a site where people can view the average breakdown of the source of their electricity along with a predicted price available on an hourly basis. We will utilize the api functions along with the models we created to predict demand to ultimately aid in predicting the electricity price for residents. The next steps will be to find sources of electricity data that we can pull on a regular basis to tune our models on and feed into a Streamlit app that end-users can interact with. We believe that giving end-users the ability to know what their electricity price will be in the future along with the composition of the sources will allow them to make informed decisions on their energy use.
