# auto-insurance-casestudy
The Vehicle Insurance company is charging the same annual premium for all the policy holders (Customer’s), irrespective of their vehicle, claim history, credit score, etc. The company wants to move towards a more dynamic pricing approach where risky drivers pay more, and less risky drivers pay less.

# Objective
Segment Customer’s into multiple groups based on their risk levels for:
• Auto insurance annual premium analysis (Dynamic Pricing approach)
• Targeted marketing campaigns

# Glossary of the Dataset
Name & Description
pol_number -  policy number for the insurance policy
pol_eff_dt - auto insurance policy effective date
gender - gender of driver: F, M
agecat - driver's age category: 1 (youngest), 2, 3, 4, 5, 6
date_of_birth - driver's date of birth
credit_score - driver’s credit score
area - driver's area of residence: A, B, C, D, E, F
traffic_index - traffic index of driver’s area of residence
veh_age - age of vehicle(categorical): 1 (youngest), 2, 3, 4
veh_body - vehicle body type
veh_value - vehicle value, in $10,000s
months_insured - number of months vehicle insurance is bought(integer)
claim_office - office location of claim handling agent: A, B, C, D
numclaims - number of claims(integer): 0 if no claim
claimcst0 - claim amount: 0 if no claim
annual_premium - total charged premium i.e. the cost of insurance

# Tools
1. Microsoft Excel
  • Initial evaluation of data
2. IDE
  • Jupyter Notebook
3. Python
  • Data Cleaning
  • Clustering/Grouping
 
The Clustering algorithms I used were:
• K-Means: In kmeans, you initialize cluster centers and then find distance between each point and each of the cluster and then you cluster points to their nearest centers. Here the optimization problem we solve is to find the no of clusters such that sum of distances from each point and its nearest cluster is minimized.
• DBSCAN: DBSCAN stands for Density Based Spatial Clustering of Applications with Noise. It groups ‘densely grouped’ data points into a single cluster. It can identify clusters in large spatial datasets by looking at the local density of the data points.
• I chose K-means as the appropriate algorithm for this dataset as it presented more detailed groups that were easier to segment.

# Results
**Cluster 1 – Older Men**
• This group consists of males who born before 1960.
• They use low range vehicles.
• Their average cost of claims is high.
Conclusion: “Above average risky drivers”

**Cluster 2 – Younger Women**
• This group consists of females who born on or after 1960.
• They use high range vehicles.
• Their average cost of claims is high
Conclusion: “High risky drivers”

**Cluster 3 – Younger Men**
• This group consists of males who born on or after 1960.
• They use mid range vehicles.
• Their average cost of claims is low.
Conclusion: “Less risky drivers”

**Cluster 4 – Older Women**
• This group consists of females who born before 1960.
• They use low range vehicles.
• Their cost of claims is average.
Conclusion: “Below average risky drivers”

# Conclusion

• K-Means gave clusters that were more precise for customer segmentation in determining their riskiness level and for marketing campaigns as well.

• There are many different clustering algorithms that could be used to cluster the drivers that are insured, but from the knowledge and tools available K-Means was found to be the best algorithm for this application.
