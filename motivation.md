---
layout: page
title: Motivation
---

**Questions**

This project develops tools for quantifying racially polarized voting in elections at all levels of the US government. Better measurement of racially polarized voting will empower organizations like the ACLU, NAACP, and thousands of local community groups to begin their own legal battles against vote dilution. To this end, we seek to answer the following questions:

1. How can we manage the noise and missing data that propagates uncertainty throughout our estimates of racially polarized voting?
2. How can we produce informative, comprehensible, and compelling visualizations of our results that can be used in court?
3. How do we integrate or use other sources of data (i.e. twitter, newspapers, school data, housing information, etc.) to improve data-driven evidence?
4. How do we ensure ethical consideration and practices while creating tools that use identifiable information?

**Background**

Why is this important?
What work has previously been done?

**Stakeholders**

Who are the important stakeholders and what has your team done to take them into consideration?
What are the use cases you’re building for?

**Ethics**

There are multiple facets of ethics our team has considered for this project. Ethical considerations must be taken into account from the moment voting registration and history data is in our possession. Furthermore, the team also considered how imprecision can have implications beyond our direct stakeholders and how results using the eiCompare package can affect various individuals and groups. We aimed to address these concerns as we completed the project.

*Voter privacy*
Firstly, we need to consider the privacy of voters. eiCompare processes voter registration and election history data from all over the country. These data files contain a great deal of information, such as names and addresses, that can be linked directly back to an individual. Although these data files are generally publicly available by filling out an inquiry form to a state or county level database, our team understood that this data should not be freely distributed and protected. We needed to protect the individuals within the databases as disseminating this information does not add to our project. Making this data freely available could lead to the nefarious use of sensitive data that may otherwise not have occurred. Data used in this project as part of examples and package development have been anonymized by removing personal information and creating an alternate unique ID. 

*Consequences of results*
Secondly, eiCompare requires multiple processing and analysis steps to assess and visualize the presence of voter dilution from raw voter files. Each step requires meticulous error handling, missing data analysis, and accuracy assessments to ensure viability of produced results.. Overestimation and underestimation of voting dilution can support or go against the narratives presented by representative constituents. However, by including checks and sensitivity analyses along the way, a user will have more confidence in their analysis and in turn will better the package’s reputation as a reliable tool. A well polished package would be indispensable for rigorous analytical work for litigation as well as inform equitable redistricting in 2021. 

*Diverse stakeholders*
Lastly, we considered the multitude of potential direct and indirect stakeholders, as well as primary and secondary stakeholders, who would be affected by eiCompare. Each individual and group has their own benefits and risks with the creation of eiCompare and the team considered the package’s impact on all of these players. As stated above, accuracy, as well as a user friendly package, benefits the greater good of the community to make just and equitable voting more attainable. Even though a courtroom may set some of these stakeholders on opposing sides, a stable analysis from eiCompare would aid in ensuring fair elections.
