# Project 4: West Nile Virus Prediction

# Problem Statement
We analyze the severity of the West Nile Virus to find the best metric to best tackle the client's request. We find that the West Nile Virus is fatal for a small proportion of the population, especially those who are older and have a weaker immune system. For the general population, about 20% of those infected will develop a fever. While this may not be fatal, those contracting the fever will have a productivity loss, and tax the city's public health services. With Covid still being prevalent, we believe that we should aim to decrease the number of WNV cases, whether it results in a fatality or a fever. As such, we believe that while our focus should be developing accurate predictions, it is just as important to maximize the number of true findings (sensitivity). 


## Background
West Nile virus (WNV) (Flaviviridae: Flavivirus) is an arbovirus circulating among mosquitoes, which serve as the vectors, and wild birds, which serve as the main reservoir hosts. WNV raises public health concerns for its ability to infect humans, which are considered dead-end hosts due to our inability to develop a sufficient viremia to infect mosquitoes. So, environmental surveillance, particularly surveillance based on mosquito sampling, can provide early detection of the virus circulation before the onset of the disease in humans.  
<br> WNV typically spreads via the bite of infected mosquitoes. Most mosquitoes do not carry the virus. While most people infected with WNV do not feel sick, about 1 in 5 people develop a fever and flu-like symptoms. Severe illness can occur in about 1 in 150 people and is most likely in people over age 60. Because there are no specific medications to treat WNV in people, the most effective method to prevent infection is to prevent mosquito bites. 
<br>
<br> So, every year, from late-May to early-October, public health workers in Chicago setup mosquito traps scattered across the city. Every week from Monday through Wednesday, these traps collect mosquitoes, and the mosquitoes are tested for the presence of West Nile virus before the end of the week. The test results include the number of mosquitoes, the mosquitoes species, and whether or not West Nile virus is present in the cohort. 

## Data and Model
The data is in a format where each row represents the results for the results of a week / trap location collection, and the interval between the dates is a week apart from May to October. The model relies on the presence of past West Nile Virus, weather data, and trap locations with a (Model) develop predictions of whether a trap will have WNV present during a particular collection week. 

The overall performance of the model depends on the AUC score and recall/sensitivity scores. Sensitivity was chosen because predicting mosquitoes to have WNV when they do not (false positives) is less of a concern than predicting mosquitoes to not have WNV when they actually do (false negatives). 


## Primary findings
The top 5 features are sunrise, temperature difference, average temperature, wetbulb temperature and station pressure. These features are not entirely surprising, since previous studies have demonstrated that features related to temperature and precipitation will make a positive impact on WNV. 


## Conclusion
Our client requested for us to provide suggestions of when and where to spray for mosquitoes which have the West Nile Virus in order to decrease their city's rate of infection and death rate. We recommend that pesticides be deployed in inner suburbs (refer to map above), and that older housing (built in the 40s-60s) be given priority due to their older sewer systems which are favourable breeding grounds for mosquito breeding. Furthermore, we recommend that spraying should be done 14 days earlier given that there is a max 14-day WNV incubation period. 

From the models developed, (Model) was selected due to several reasons:
* The model was built based on feature reduction. This allowed us to filter irrelevant or redundant features based on domain knowledge; It is a relatively safe technique to ensure that the features that have been 'proven' to possess high predictive power to be included in the model. 
* Highest roc_auc accuracy.  The model provide good predictions and could provide an accurate distinguish between the classes. 
* The model has high sensitivity, ie., the model has low false negatives. Since predicting mosquitoes to have WNV when they do not (False Positives) is less of a concern than predicting mosquitoes not to have WNV when they actually have it (false negatives). 


