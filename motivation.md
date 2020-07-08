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

In the spring of 2020, the NAACP won a landmark voting rights case in the East Ramapo School District of Rockmount County, New York by convincing the judge that precinct boundaries drawn for school board elections substantially diluted the Black and Latino minority vote. Vote dilution violates Section 2 of the Voting Rights Act (VRA), which “prohibits drawing election districts in ways that improperly dilute minorities’ voting power.”

Expert witnesses in the case used a wide array of novel data science methods to quantify vote dilution, and their victory cemented the validity of these tools in a legal setting and future voting rights litigation.

In this DSSG project, we are improving upon and making the techniques they used accessible to everyone, so that groups and organizations throughout the country can fight for their electoral rights. 

![Image 1. Decelle (2017) "Students of the East Ramapo School District hold a sign during the One Voice United Rally in Albany". Retrieved July 7, 2020 from The Atlantic website: https://www.theatlantic.com/education/archive/2017/11/another-blow-to-one-of-americas-most-controversial-school-board/546227/ .](images/eastramapo_schooldistrict_rally_theatlantic.jpg)

Without fair representation, minority citizens cannot effectively support and protect their own institutions such as education. In the East Ramapo case, lawyers from the New York Civil Liberties Union (NYCLU) explained how dilution of Black and Latino votes in school board elections led to the gradual siphoning of funds from public schools attended by Black and Latino students to private schools attended by white students. As a result, the educational experiences of public school attendees began to deteriorate:

  * “The board eliminated hundreds of public school teaching, staff, and administrative positions and eliminated classes and programs”

  * “Public school buildings fell into disrepair and custodial services were reduced”
  * “Students were given academically deficient schedules full of free time and filler”
  * “The board closed two public schools over minority opposition”
  * “Graduation and test scores sank”

To convince the judge that the defunding of public schools ultimately resulted from vote dilution, the plaintiffs’ evidence needed to pass the Gingles Test, established as precedent for assessing minority vote dilution in the 1986 case Thornburg v. Gingles. The Gingles test requires showing:

  1. The group of minority voters is sufficiently large and geographically compact
  2. Minority voters are politically cohesive in supporting their candidate of choice
  3. The majority votes in a bloc to usually defeat the minority’s preferred candidate


Voting dilution can be difficult to prove because voting is confidential - we can never know who voted for which candidate with certainty. However, new innovations in quantitative social science can now provide data-driven evidence to meet the requirements needed to pass the Gingles test.  These methods include ecological inference and Bayesian Improved Surname Geocoding (BISG). 


Ecological inference (EI) takes aggregate and historical (ecological) data to infer individual behavior (King, 1997). BISG uses demographic data (i.e. surnames, racial identity, and geographic data) collected from the United States Census Bureau, along with, field-specific data like voter information to predict the race or ethnicity of each person in the sample population (Elliott et al. 2019). Current research further examines the methods of ecological inference and BISG through creating and updating existing software (built in R) that specifically calculates the probability of race or ethnicity for individuals and executes the process of EI for detecting voting dilution (Barreto et al. 2019, Collingwood et al. 2016).



References:

1. Barreto, M., Collingwood, L., Garcia-Rios, S., & Oskooii, K. A. (2019). Estimating Candidate Support in Voting Rights Act Cases: Comparing Iterative EI and EI-R× C Methods. Sociological Methods & Research, 0049124119852394.

2. Collingwood, L., Oskooii, K., Garcia-Rios, S., & Barreto, M. (2016). eiCompare: Comparing Ecological Inference Estimates across EI and EI: RC. R J., 8(2), 92.

3. Elliott, M. N., Morrison, P. A., Fremont, A., McCaffrey, D. F., Pantoja, P., & Lurie, N. (2009). Using the Census Bureau’s surname list to improve estimates of race/ethnicity and associated disparities. Health Services and Outcomes Research Methodology, 9(2), 69.

4. King, G. (1997). A solution to the ecological inference problem: reconstructing individual behavior from aggregate data. Princeton: Princeton University Press.


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
