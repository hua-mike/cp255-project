# San Francisco Crosswalks: Safety and Inequities
### Mike Hua
#### CYPLAN 255: Urban Informatics and Data Visualization
#### Spring 2022

# Introduction

In San Francisco, CA, there are around 30 traffic deaths and over 500 serious injuries each year. The City of SF, like many cities around the world, is pursuing a Vision Zero goal to have zero traffic deaths. Painted crosswalks are among the most basic forms of pedestrian infrastructure. Adding crosswalks is listed in SF's Vision Zero plan as a low-cost measure to increase safety.

# Analysis

This analysis builds upon the work of Marcel Moran, Ph.D. Candidate in City and Regional Planning at UC Berkeley. Moran published a study mapping crosswalk coverage at all intersections in San Francisco ([Moran, 2022](https://escholarship.org/uc/item/67447864)). Moran manually reviewed satellite imagery of the roughly 6,400 intersections in SF and recorded whether all pedestrian crossing had a painted crosswalk. The study used a binary "crosswalk" or "no crosswalk" designation"—if any crosswalks were missing from an intersection, it was marked as "no crosswalk". The paper for the study describe in further detail the methodology used and assumptions made.


## Inequitable Distribution of Crosswalks

Only 58% of intersections in San Francisco have full crosswalk coverage. Mapping out intersections with and without fully marked crosswalks shows a clear spatial disparity between the northern and southern areas of the city.

<img src="images/crosswalks.png" width=150%>

The below hexbin map further illustrates the spatial disparities of crosswalks in the city. Using arbitrary hexagonal geometries helps mitigate against potential error from the [Modifiable Areal Unit Problem](https://gisgeography.com/maup-modifiable-areal-unit-problem/). This map again shows that southern portions of SF have lower crosswalk coverage.

![](images/cw-hexbin.png)

The below map shows crosswalk coverage by Supervisor District (the SF Board of Supervisors is the legislative body of the city). Again, intersections in the southern supervisor disctricts of SF are much less likely to have fully marked crosswalks. The disparity by supervisor district might also allude to differences in political power of districts to get infrastructure improvements, however further analysis is needed.

<img src="images/sup-district.png" width=150%>

## Priority Crosswalk Installation

# Results

# Discussion

From my initial analysis of the crosswalk audit data, its clear that there are spatial disparities in marked crosswalks. Northern areas of the city typically have more intersections with fully marked crosswalks than the southern areas of the city.

# References