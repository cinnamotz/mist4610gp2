# MIST 4610 Group Project 2 - Group 7

## Group Members:

1. Donovan D'Silva - 	[repo](https://github.com/donmelsil/MIST-4610-Group-Project-2---Group-7)
2. Noah Hammond	-[repo](https://github.com/NoahHammond1/Group-Project2)
3. Chase Lin - [repo](https://github.com/cinnamotz/mist4610gp2)
4. Krithin Lokasani	- [repo]()
5. Jessica Ngo -[repo](https://github.com/jn83499/Mist4610_Group-Project2)

## Dataset and Description
The dataset, titled “NYPD Hate Crimes”, contains records of reported hate crime incidents investigated by the New York Police Department (NYPD). Each row represents a single complaint, including details about the offense, location, bias motivation, and whether an arrest was made.

Dataset was obtained from Data.gov (https://catalog.data.gov/), the U.S. government’s open data portal. It aggregates datasets from federal, state, and local agencies, and this dataset originates from the NYPD as part of New York City’s public data initiatives.

Number of rows: 4,029

Number of columns: 14

Each row corresponds to one reported hate crime complaint.

The dataset contains a mix of numerical and categorical variables, making it suitable for both statistical and categorical analysis. Several fields related to arrests contain missing values, indicating incidents where no arrest was made. The data supports analysis of temporal trends, geographic distribution, and bias motivations behind hate crimes.

Overall, this dataset provides a comprehensive view of hate crime incidents in New York City, including when and where they occurred, the type of offense, and the underlying bias motivation. Its structure makes it well-suited for exploratory data analysis and identifying patterns in hate crime activity.

### Columns and Data Types
1. Full Complaint ID (float64): Unique identifier for each complaint.
2. Complaint Year Number (int64): Year the complaint was filed.
3. Month Number (int64): Month of occurrence (1–12).
4. Record Create Date (string/object): Date the record was entered into the system.
5. Complaint Precinct Code (int64): Numeric code for the NYPD precinct.
6. Patrol Borough Name (string/object): Borough-level patrol division.
7. County (string/object): County where the incident occurred.
8. Law Code Category Description (string/object): Legal classification (e.g., felony, misdemeanor).
9. Offense Description (string/object): General type of crime.
10. PD Code Description (string/object): Specific NYPD classification of the offense.
11. Bias Motive Description (string/object): Motivation behind the hate crime.
12. Offense Category (string/object): Broader grouping of offenses.
13. Arrest Date (float64 / nullable): Date of arrest, if applicable.
14. Arrest Id (string/object): Identifier for associated arrest, if any.

## Questions

Question 1:

How does the total number of misdemeanor and felony hate crimes vary across boroughs over time?

Why it’s important:
This question is important from a social and public safety perspective because it helps identify which boroughs experience higher levels of hate crime activity and whether those patterns are changing. Tracking this over time can reveal whether certain communities are becoming safer or more at risk.

From an economic standpoint, boroughs with consistently higher crime levels may face reduced investment, lower property values, and negative impacts on local businesses.

Connection to dataset:

Complaint Year Number → captures time trends
Patrol Borough Name / County → identifies geographic distribution
Law Code Category Description → filters for misdemeanors and felonies

## Data Manipulations and Calculations

To conduct the analysis, several key data manipulations were performed:

Filtering
The dataset was filtered to include only records where Law Code Category Description = “Misdemeanor” or “Felony”.
Purpose: Focus the analysis specifically on offense severity and exclude violations or other categories.
Grouping and Aggregation
Data was grouped by:
Borough (Patrol Borough Name or County)
Year (Complaint Year Number)
Offense Type (Misdemeanor vs. Felony)
A count of incidents was calculated for each group.

Purpose:
This allows comparison of total offenses across boroughs and years while distinguishing severity.

A calculated field was created to standardize offense categories (e.g., grouping variations into “Misdemeanor” and “Felony”).
Another calculation could include total offenses per borough-year combination.

Purpose:
Ensures consistency in categorization and enables accurate aggregation for visualization.

Visualization Preparation
Data was structured to support a color-coded visualization by year (e.g., using year as a color legend).

Purpose:
This allows clear visual comparison of trends over time within each borough.

3. Analysis and Results
Visualization Description

The results were visualized using a grouped bar chart (or heatmap):

X-axis: Boroughs
Y-axis: Total number of hate crime incidents
Color coding: Year
Separate bars or segments distinguish misdemeanors vs. felonies
Key Findings

1. Uneven Distribution Across Boroughs
Certain boroughs consistently show higher total counts of hate crimes (both misdemeanors and felonies), indicating geographic concentration.

Implication:
This suggests the need for targeted law enforcement and community outreach programs in specific areas.

2. Felonies Are Less Frequent but More Concerning
While misdemeanors make up a larger share of incidents, felonies—though fewer—represent more severe crimes.

Implication:
Even small increases in felony counts are significant and may indicate escalating violence or risk.

3. Year-to-Year Fluctuations
Color-coded trends show that hate crime incidents vary by year, with some boroughs experiencing spikes or declines.

Implication:
These fluctuations may be linked to external social or political events, highlighting the importance of continuous monitoring.

4. Variation in Severity by Borough
Some boroughs show a higher proportion of felonies relative to misdemeanors compared to others.

Implication:
This could indicate differences in crime dynamics, enforcement practices, or underlying social tensions across boroughs.

4. Overall Implications

This analysis provides a multidimensional understanding of hate crime patterns, combining:

Geographic insights (borough-level differences)
Temporal trends (changes over time)
Severity analysis (misdemeanor vs. felony)

These findings are valuable for:

Law enforcement agencies → better resource allocation
Policymakers → informed decision-making and interventions
Communities → increased awareness and advocacy
