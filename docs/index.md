# San Francisco Crosswalks: Safety and Inequities
### Mike Hua
#### CYPLAN 255: Urban Informatics and Data Visualization
#### Spring 2022

# Introduction

In San Francisco, California, there are around 30 traffic deaths and over 500 serious injuries each year. The City of SF, like many cities around the world, is pursuing a Vision Zero goal to have zero traffic deaths. Painted crosswalks are among the most basic forms of pedestrian infrastructure. Adding crosswalks is listed in SF's Vision Zero plan as a low-cost measure to increase safety.

# Analysis

This analysis builds upon the work of Marcel Moran, Ph.D. Candidate in City and Regional Planning at UC Berkeley. Moran published a 2022 study mapping crosswalk coverage at all intersections in San Francisco ([Moran, 2022](https://escholarship.org/uc/item/67447864)). Moran manually reviewed satellite imagery of all intersections in SF jurisdiction (about 6,400) and recorded whether all pedestrian crossings had a painted crosswalk. The study used a binary "crosswalk" or "no crosswalk" designation"—if any crosswalks were missing from an intersection, it was marked as "no crosswalk". A manual review was chosen because available data from city agencies was not comprehensive for all intersections in SF. The full text of the study describes in further detail the methodology used and assumptions made by the researcher.

This project aims to continue to study the spatial disparities of crosswalk coverage, as well as begin the process of developing a prioritization metric that can help SFMTA (the city department of transportation in SF) understand which missing crosswalks should be given prioritized consideration for crosswalk installation.

## Inequitable Distribution of Crosswalks

42% of intersections in San Francisco are missing full crosswalk coverage. Mapping out intersections with and without full crosswalk coverage shows a clear spatial disparity between the northern and southern areas of the city.

<img src="images/crosswalks.png" width="2000">

The below hexbin map further illustrates the spatial disparities of crosswalks in the city. Using arbitrary hexagonal geometries helps mitigate against potential error from the [Modifiable Areal Unit Problem](https://gisgeography.com/maup-modifiable-areal-unit-problem/). This map again shows that southern portions of SF have lower crosswalk coverage.

![](images/cw-hexbin.png)

The below map shows crosswalk coverage by Supervisor District (the SF Board of Supervisors is the legislative body of the city). The north/south disparity remains clear: intersections in the southern supervisor districts of SF are much less likely to have fully marked crosswalks. The disparity by supervisor district might also allude to differences in the political power of districts to get infrastructure improvements, however further analysis is needed.

<img src="images/sup-district.png" width="2000">

## Priority Crosswalk Installation

The high injury network (shown below in blue) is defined by the SF Vision Zero team and SF Public Health as the highest-concern streets for traffic injuries. The network represents the 12% of streets where over 70% of collisions occur.

![](images/hi-injury.png)

The below map with all missing crosswalks overlaid on the high injury network does not show an observable spatial relationship.

![](images/hi-inj-no-cw.png)

Equity Priority Community is a designation created by the Metropolitan Transportation Commission (MTC), the regional planning agency for the SF Bay Area, to identify areas that have historically marginalized and underserved groups. Many SF and regional agencies use the Equity Priority Community framework to help prioritize transportation investments. MTC's GitHub page contains [details on the Equity Priority Community definition](https://bayareametro.github.io/Spatial-Analysis-Mapping-Projects/Project-Documentation/Equity-Priority-Communities/).

![](images/epc.png)

Overlaying the high injury network and Equity Priority Communities can help narrow down which missing crosswalks should be prioritized by the city. The dots shown here are all missing crosswalks that are on the high injury network and within an Equity Priority Community

![](images/no-cw-on-injnet-epc.png)

Further narrowing of the set of priority missing crosswalks can be achieved by selecting intersections that have had a recent pedestrian collision. Data was used from the California Statewide Integrated Traffic Records System (SWITRS), accessed via UC Berkeley's SafeTREC lab (Safe Transportation Research and Education Center). The below map depicts all crashes involving pedestrians from 2015 to 2019. This time frame for the data was chosen because the 2020 and 2021 data were still provisional at the time this analysis was conducted.

![](images/crashes.png)

This data was used to select only missing crosswalks that have had at least one pedestrian collision from 2015 to 2019. A total of 28 intersections in San Francisco meet all four criteria:

1. At least one crossing in the intersection is missing a painted crosswalk
2. The intersection is on the high injury network
3. The intersection is within an Equity Priority Community
4. The intersection has had at least one pedestrian collision recorded in the past 5 years of available data (2015 - 2019).

![](images/no-cw-on-injnet-epc-1crash.png)

This smaller set of 28 crosswalks is a more manageable quantity for city agencies to further analyze. Within this set, there are 4 intersections with 2 or more collisions, located at Washington St & Waverley Pl in Chinatown, both 16th St & Caledonia St and 16th St & Hoff St in the Mission District, and 6th St and Shipley St in SoMa. All of these are 3-way intersections where smaller alleys meet larger arterials, which might suggest a need for crosswalks for small streets located next to arterials.

This prioritization metric is intended as a starting point to begin conversations about which crosswalks are needed to be installed. City agencies will need to take a detailed look at each identified intersection to assess the current safety of the design and determine if installing a crosswalk is a worthwhile investment in comparison to other potential crosswalk installation sites.

In addition, crosswalks are just one piece of the puzzle for pedestrian safety. Other infrastructure improvements like leading pedestrian intervals and curb bulb-outs were not analyzed in this project, but are critical measures to take to get to Vision Zero goals. A cohesive approach involving a variety of strategies will be needed to achieve Vision Zero.

# Conclusion

From this exploratory analysis of the crosswalk audit data, it is clear that there are spatial disparities in marked crosswalks in San Francisco. Northern areas of the city typically have more crosswalk coverage than southern areas.

The City of San Francisco should work to address missing crosswalks at critical intersections and work to reduce the inequitable distribution of crosswalk coverage. The described crosswalk installation priority analysis would help the city prioritize crosswalks that are on high-injury streets and in historically-underserved areas that deserve prioritized investment. Understanding existing disparities in pedestrian safety and targeting investments to address those disparities is critical to equitable progress toward Vision Zero safety goals.

# References

Moran, M. E. (2022). Where the Crosswalk Ends: Mapping Crosswalk Coverage via Satellite Imagery in San Francisco. Environment and Planning B: Urban Analytics and City Science, 23998083221081530. https://doi.org/10.1177/23998083221081530

