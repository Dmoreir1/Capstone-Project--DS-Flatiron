# Demand for Charging Stations by predicting EV's on road using time series forecast
## Dan Moreira - Flatiron Data Science capstone project



### Data Source: [AtlasEVHub](https://www.atlasevhub.com/materials/state-ev-registration-data/#data)

##### This project is hypothetical and for educational purposes * 

![pexels-kindel-media-9800029](https://user-images.githubusercontent.com/103558721/200761713-fe8c330f-82f8-43a4-b0c3-96240e0136bd.jpg)

## Introduction


Electric Vehicles or 'EV's are the future of transportation. In addition to a mindset of environmental sustainability, state governments are offering incentives for people who are purchasing/registering electric cars in hopes of promoting this shift from reliance on fossil fuels. 
Unlike traditional gas cars, these vehicles rely on battery power and need to be charged in order to operate. 
With more and more electric vehicles on the road, an opportunity for investment presents itself as there is an increasing demand for charging stations. But which states would be best to invest in?

Elon Musk is looking to invest more in charging station infrastructure and has asked my team to determine which state(s) would be most lucrative outside of California and Texas as he already has large presence in these states. 




![elon-musk-space2](https://user-images.githubusercontent.com/103558721/202408006-f58e7fff-9c04-40f2-a08e-2066931a004d.jpeg)

## Objective

![pexels-jack-s-9469484](https://user-images.githubusercontent.com/103558721/200761647-73522609-3450-43a1-bc56-66a1368d2316.jpg)

Using DMV data dating back from the past 10 years from 16 states (CA, NY, NJ, CT, TX, FL, MT, MN, MI, WA, OR, VT, VA, TN CO, WI) that have been actively updating their records for registered EV's, I have modeled each state to figure out the fastest growing by forecasting the quantity of registered vehicles on the road.

Which states are forecasted to have the highest growth in Battery Powered Electric vehicles that would have high demand / be ideal candidates to invest in for charging station infrastructure? 

![pexels-kindel-media-9799996](https://user-images.githubusercontent.com/103558721/202411541-50df81e6-7ec5-4cb9-a1c7-8cac92c9eef9.jpg)

## Methodology 

1) Using state DMV snapshots, narrowed down results to only include vehicles that require charging stations or BEV's (Battery Electric Vehicles) 
2) Used the 'Registration Valid Date' from records to create time series 
3) Due to upwards trend in data, utilized SARIMA modeling to account for seasonality
4) Used train/test split to validate performance of data (Confidence Interval of 95)
5) RMSE to evaluate performance
6) Forecasted amount of registered vehicles on road for 2025 

![dcbel-7aFmUOkguyE-unsplash](https://user-images.githubusercontent.com/103558721/202411613-603c418d-6c08-43a1-9f73-9c48f4ae7623.jpg)


## Limitations 

- Availability of data as not every state updates frequently or leaves readily accessible
- Limited historic data to create model (several states with dating back only 4-5 years) as EV's are still fairly recent/new
- Limited access to VIN numbers as they are personal data; had to consider that some vehicles in records may be recorded more than once


## Takeaway
We found in our research that the states exhibiting the highest growth in Battery Powered EV's (outside California and Texas) are Florida, New Jersey and New York. 

![tesla charging station](https://user-images.githubusercontent.com/103558721/202411736-05d9e19d-4029-437e-ae9f-bbabed4d4ebb.jpeg)


## Modeling


![florida validation model](https://user-images.githubusercontent.com/103558721/202411782-82223aa3-b4ea-45f6-985d-c85e275902c5.png)

![New Jersey validation model](https://user-images.githubusercontent.com/103558721/202411800-7bb470e8-1d1a-4da9-bda7-0f52a8a84131.png)

![New York validation model ](https://user-images.githubusercontent.com/103558721/202411809-5a93b64d-9e7b-4aa2-b00c-9dd223ee9969.png)

** Due to the pandemic's effect on NY's population and the DMV's reporting frequency, we saw a decline where we predicted strong upwards growth.



## Forecasting/Deployment


![Florida EV battery forecast](https://user-images.githubusercontent.com/103558721/202412048-e6b19ac2-d7a0-46e8-accb-e3dc1adc90c6.png)
![NJ EV Battery forecast](https://user-images.githubusercontent.com/103558721/202412072-464933aa-1df3-4caa-bd44-9fa02b8cee2b.png)
![New York forecast ev](https://user-images.githubusercontent.com/103558721/202412082-46c95293-01b4-4559-a233-99444e8d8f26.png)



## Recommendations 

Tesla's market share in: 

1) Florida 61.41% of EV market with 55,370
2) New Jersey 57.4% of EV market with 36,182
3) New York 38.84% of EV market with 39,070

We recommend for Tesla to invest in Florida and New Jersey as both states exhibit substantial growth by 2025 in EV driver population as well as already having the dominant market share in these states 

* Consider the universal compatibility for charging stations to be used with other EV's 


![rick-govic-rLTjEVGXNBA-unsplash](https://user-images.githubusercontent.com/103558721/202413672-f1a1f4e4-7ead-45da-9fe6-c4f238d12aa0.jpg)

## Future Considerations 

1) Revisit data and using a vin decoder to apply additional filters for battery types and investigating compatibility of chargers.

2) Utilize deep learning (eg. tensorflow)

3) Further analyses on data that accounts for state registrations expiration dates and remove any duplicate entries 


Additional Sources: 
https://afdc.energy.gov/fuels/electricity_infrastructure.html
https://www.duke-energy.com/energy-education/electric-vehicles/charging-your-ev/types-of-chargers
https://www.atlasevhub.com/wp-content/uploads/2022/05/Open-Vehicle-Registration-Initiative.pdf
https://www.iea.org/data-and-statistics/data-tools/global-ev-data-explorer
https://www.nature.com/articles/s41597-021-00932-9
https://climatebiz.com/cost-of-an-ev-charging-station/
https://www.kbb.com/car-advice/ev-charging-stations/
