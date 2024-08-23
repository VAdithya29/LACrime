# 👮 Crime Prediction 👮

## Introduction
Between 2020 and 2023, nearly a MILLION crimes were reported in the city of Los Angeles, a staggering figure. And these are just the reported incidents. The thought of how many more crimes may have gone unreported is truly chilling.  
The aim of this project is to determine just how predictable everyday crimes can be.  
By analyzing patterns and trends, we aim to provide valuable insights that could help law enforcement anticipate and prevent future incidents.  
The ultimate goal is to equip authorities with the data-driven strategies they need to combat and reduce these alarming crime rates, making communities safer and more secure.

## Dataset
The Los Angeles crime dataset covers incidents from 2000 to May 2024, detailing crime dates, times, locations, and types, along with victim demographics and suspect behaviors. 
It includes geographic information tied to LAPD's 21 community areas, crime codes, weapon details, and case statuses. This comprehensive data is crucial for analyzing crime patterns and developing strategies to enhance public safety.
The dataset can be found on LA City's website on <a href="https://data.lacity.org/Public-Safety/Crime-Data-from-2020-to-Present/2nrs-mtv8/data">here</a>.

## Methodology
### Libraries and Packages used: 
| Language | Libraries Used |
|----------|----------------|
| R        |dplyr, ggplot2, plotly, lubridate, caret                |
| Python   |tensorflow keras, scikit-learn, matplotlib, pandas, numpy, datetime                |

Data was first cleaned and processed to include only the relevant data for each model.  
Data was split into 3 parts, based on the range considered.  
2. Year 2020-2023, All Types of Crimes  
2. Years 2020-2023, Top 10 Types of Crimes  
3. Year 2023, All Types of Crimes  
4. Year 2023, Top 10 Types of Crimes  
Individual Jupyter notebooks for all these are included in the repository.  
**Please note that the files may take upto 3 hours to run due to the neural networks being slow. You can can comment it out and run just the random forest. The wait time should be much shorter.**  
Random Forest and Neural Network models were fitted for all each of these and the results were checked to select the best model.  
SVM and Gradient Boosting were also tried out but failed to provide satisfactory results.  

## Results
This is a comparison table of the results we got from using the Random Forest and Neural Networks.

|                        | Random Forest                 || Neural Networks                 ||
|------------------------|:-------------:|:--------------:|:---------------:|:--------------:|
|                        | With L&L      | Without L&L    | With L&L        | Without L&L    |
| 2020-23, Top 10        | 26.19         | 19.46          | 26.32           | 26.29          |
| 2023, All Crimes       | 18.8          | 18.97          | 18.85           | 19.04          |
| 2023, Top 10           | **28.68**         | 27.06          | 26.77           | 27.06          |

As we can see, the Random Forest Test that predicts only the top 10 types of crimes that occured in 2023, performed the best.  
Overall, all models that predicted streamlined data worked the best, but there was not a huge dropoff when comparead against models that considered data for all 4 years, meaning, it is a tradeoff.  

## Future Scope
- Enhanced Crime Prediction Models  
- Implementing models that can detect emerging crime hotspots in real-time  
- Using insights from the data to inform and develop more effective crime prevention strategies tailored to specific areas or types of crime  
- Integrating the crime prediction system with IoT devices and smart surveillance systems in cities to enhance real-time monitoring and response  
- Facilitating data sharing and collaboration between law enforcement agencies, municipalities, and research institutions to improve crime prediction and prevention strategies  
- Conducting studies to assess the impact of predictive policing and hotspot detection on actual crime rates and community safety over time
