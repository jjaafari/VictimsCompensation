# VictimsCompensation
A data investigation into six states' victims compensation reimbursement program
<hr>
<h1>SUMMARY:</h1>

Though states’ compensation funds dole out millions of dollars each year, there is a litany of reasons why families of homicide victims can be denied. One of the most controversial is known as “contributory conduct,” which allows a state to deny funds to a victim’s family if it’s determined that the person killed was in some way responsible for their own death.

Whether or not a victim engaged in contributory conduct is a determination made by homicide detectives. And while a murder victim’s actions at the time of death can be helpful in catching the killer, rarely are they ever used in court as evidence for the perpetrator’s motive. Contrast that with claims to victims’ compensation funds, where the behavior of the deceased is a primary driver of whether a family member will receive money. 

An investigation by NationSwell looked at county data in six states — Arizona, New Jersey, Louisiana, New York, Pennsylvania and Texas — which showed that thousands of families are denied compensation each year because of the contributory conduct clause. 

Regulators involved in processing claims say they are just following federal law and that there needs to be top-down change in order for there to be significant progress on the best way to assist financially strapped families. But one victims’ services group in Philadelphia, the city with the highest number of compensation claims filed each year in Pennsylvania, is helping families navigate the system and fight for their right to fair treatment. 

<h2>REPORTER’S NOTE:</h2>

I was first approached by Chantay Love, the main subject of our accompanying video, about this story in 2015. We were discussing reimbursement for families who were paying for blood cleanup after a murder or a shooting occurred in their home (blood cleanup can cost thousands, but families can only get reimbursed hundreds). 

Love, the program director of Every Murder Is Real Healing Center, was working out of EMIR’s office in the basement of a church in the Germantown section of Philadelphia. She was determined to explain to me how the state’s Victims Compensation Assistance Program was systematically denying poor families the money they were entitled to by law — most of them families of color. 

But the data to prove there was pattern to the denials wasn’t there at the time, and what data I did get from the Pennsylvania Commission on Crime and Delinquency didn’t show much more than the fact that denials were happening, no matter the cause. 

I started to look for a pattern months later when Love reached out again and said she wanted me to speak with family members of murder victims. She put me in touch with a father whose son was shot trying to smooth over a street fight, and he was denied reimbursement because there was an allegation that his son had been dealing drugs. 

At the same time, I met Amy Albert, a lawyer in New Jersey who was working on this problem with a handful of mothers in her Jersey City neighborhood. She made the same claims that Love had when we first met: Namely, that poor black families affected by crime are being denied state funds because of alleged criminal activity on the part of the victim. But there was no due process given to those that have died. And since crimes are -— more often than not — enmeshed with poverty, there was an economic bias in the regulations that could allow white families to be treated differently.

There were immediate questions I had: How many people were actually being denied? Who were the people getting denied, and for what reason? And were the reasons actually based on racial bias? 

After conducting a bit of cursory research, I realized this compensation denials were not unique to Pennsylvania or even New Jersey — this was something that was happening everywhere. 

<h2>WHAT WE WERE ABLE TO GET:</h2>

A large portion of the data we used has been made available to the public online by state offices, albeit mostly in image-based PDF form. The data we have uploaded here is cleaned, organized and processed. 

NationSwell made the decision early on to work with as much public information as possible, filling in any holes later by filing requests with state officials. But ultimately, we wanted to show a pattern of denials existed based off what was being disseminated to the public.

In reality, given the timeline of when we wanted this story to be completed, we had to rely on the fact that Freedom of Information requests were not going to be fulfilled in a timely manner. 

One of the biggest hurdles we faced is that state victims’ compensation offices are only required to report what the federal Office for Victims of Crimes outlines. For many years, the basic requirements only included data such as total claims filed, claims denied, claims paid out and monetary disbursements. 

These requirements changed every year. Some states, like New Jersey, had been filing denials by county as far back as 2010. Louisiana was doing the same while also providing the number of denials based on contributory conduct. But because the federal office hadn’t mandated that states’ reports include contributory conduct denials by county until recently, some states, like Arizona, had yet to begin breaking down denials by county, which led to incomplete data sets. 

In the end, what we got was a lot of tables containing empty rows, because every state filing is different. 

What we were able to maintain constant at the county level: 

<i> No. of claims filed, No. of claims paid, Amount paid per year, No. of denials</i>

At the state level, more variables held constant, including in addition to the above:

<i>Denials based on contributory conduct, Funeral payouts </i>

For each state we analyzed, we gathered data from the years 2010 through 2017. But to do a  state-by-state comparison, we had to limit ourselves to figures from 2013 to 2015, where we had the most complete data sets. 

<h2> DEFINITIONS AND PROCESS:</h2>

Average Processed per year:
This value is the number of claims processed per county averaged over the three years from 2013–2015.

Total Processes for all years:
This value is the number of claims processed per county totaled over the three years from 2013–2015.

Percent Denied/Percent of Claims Denied:
To calculate the average percent of claims denied, counties named the following were removed from the analysis: “Other”; “No County”; and “Out of State.” The data was grouped by county and state, and the percent of claims denied for 2013–2015 was calculated as the sum of annual claims denied divided by the sum of annual claims processed. This give one value for the entire time period, rather than an average of the three years. This choice was made due to the rolling nature of processed claims and to avoid giving each of the three years significant leverage over the final value. For a given county, if the number of claims processed varied notably across the three years, an average would not capture that. For these reasons, the decision was made to aggregate numbers over the three-year period rather than average them.

Total Denied:
This value is the number of claims denied per county totaled over the three years from 2013–2015.

Average Number Paid:
This value is the number of claims paid per county averaged over the three years from 2013-2015.

Total Number Paid:
This value is the number of claims paid per county totaled over the three years, 2013-2015.

Percent Unpaid:
This value is the number of claims processed minus the number of claims paid, divided by the number of claims processed over the three-year period.

Percent nonwhite:
The percentage of nonwhite residents was calculated as 100 minus the percentage of white residents according to the 2010 census.

Relationship Between Minority Population and Claims Denied:
To understand this relationship, a county-level regression model was built that included multiple explanatory variables. The counties were treated as single observations, with the three years of observations aggregated for each county. Counties with fewer than an average of 20 claims per year were excluded, because counties with so few claims are likely to review them differently than counties with higher volumes of claims to process each year. The model focused on the explanatory variable “percent nonwhite” and included “state” and “total claims processed” as controls. In order to achieve linearity in the model, the dependant variable was transformed as the logarithm of total denials. This allowed for an interpretation of “percentage change” between the percent of nonwhite residents and the total denials. The model resulted in the following:

Call:
lm(formula = log(total_denied) ~ percent_nonwhite + factor(State) + 
    log(total_processed_all_years), data = counties_with_race)

Residuals:
Min       	1Q   		Median       	3Q      		Max 
-0.79475 	-0.15894  	0.02306  	0.14006  	0.68173 

Coefficients:
<table>
  <tr>
    <th></th>
    <th>Estimate Std.</th>
    <th>Error</th>
    <th>t value</th>
    <th>Pr(&gt;|t|)</th>
  </tr>
  <tr>
    <td>(Intercept)</td>
    <td>-2.699431</td>
    <td>0.147517</td>
    <td>-18.299</td>
    <td>&lt; 2e-16 ***</td>
  </tr>
  <tr>
    <td>percent_nonwhite</td>
    <td>0.003899</td>
    <td>0.001280</td>
    <td>3.045</td>
    <td>0.00289 **</td>
  </tr>
  <tr>
    <td>factor(State)Louisiana</td>
    <td>0.334160</td>
    <td>0.126859</td>
    <td>2.634</td>
    <td>0.00961 **</td>
  </tr>
  <tr>
    <td>factor(State)Texas</td>
    <td>0.721242</td>
    <td>0.089263</td>
    <td>8.080</td>
    <td>7.53e-13 ***</td>
  </tr>
  <tr>
    <td>log(total_processed_all_years)</td>
    <td>1.039189</td>
    <td>0.021546</td>
    <td>48.231</td>
    <td>&lt; 2e-16 ***</td>
  </tr>
</table>

Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.2659 on 114 degrees of freedom
Multiple R-squared:  0.9633,	Adjusted R-squared:  0.962 
F-statistic: 748.4 on 4 and 114 DF,  p-value: < 2.2e-16

The coefficient on percent_nonwhite is interpreted as: for a unit increase in the percent of nonwhite residents, the percent of denials increases by 100*(e^(0.003899)-1)=.39%.  So, holding state and total claims processed constant, for every 10% increase in the percent of nonwhite residents, percent of denials increases by about 4%.

<h2>WHAT WE LEFT OUT (AND WHY):</h2>

One of the things we were worried about was that with social issues, it’s hard to show cause and effect. We had the data to show a direct link between the racial makeup of a county and the number of denials, but we were facing a bigger problem: Was there, in fact, evidence of a causal link?

The short answer was no. Although we initially felt that what victims’ advocates were telling us might be right, we couldn’t find any empirical evidence of a relationship between denials and racial makeup. 

This is why, though, we looked at county racial data. For every county we looked at, we identified 2010 census numbers of non-Hispanic white populations versus other minority populations. 

This is not the best way to show a relationship of racial injustice, we readily admit. However, it gave credence to the argument that almost every advocate had been telling us: that black families were getting denied more often than white families. 

We had every intention of showing a scatter plot and trend curve that would’ve also proven that point, but conceded in the end that it would’ve misled the audience. Using an x and y axis to denote a trend shows causation, when what we found was more correlation — which we acknowledged from the beginning. 

(Big thanks to NICAR folks for talking us out of that bad decision.)


<h2>WHAT WE HOPE FOR:</h2>

We hope some other outlets with more resources are able to take the data that we’ve compiled so far and run with it. At NationSwell, we don’t have the resources to dedicate years to an investigation (it was hard enough to work for five months on this one). And we also don’t have the full data reporting hub that is needed to fully dig into this properly. That said, we’ve made all of the data we collected publicly available for download on this GitHub, in the hopes that this knowledge can further a conversation about assumptions of guilt and victims’ rights in the U.S. 

<h3>Reporter:</h3>
Joseph Darius Jaafari, joseph@nationswell.com

<h3>Data Scientist:</h3>
Malorie Hughes, mhughes@npr.org

