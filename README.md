# Childcare Cost & Affordability Dashboard
![Family](https://github.com/canistag/childcare/blob/main/family%20visualizer.png)

## Description 
A dashboard that visualizes the cost of supporting a family across all fifty states of the US. 
## The Question
- How much money is needed annually to comfortably have a family in each state?
- What are the most and least expensive places to have a family?
## Assumptions
An assumption I have made is that the average family consists of two parents, two children, a dog, and a cat. In addition to this, each family will have two insured, paid off cars, a 3 bedroom 2 bathroom house, and a 401k fund for each parent. For the children, each will have a sport and extracurricular, a Roth IRA savings account, and a 529 college savings account. Each of these funds and or savings accounts will be a recurring expense of $100 each per month ($1200 annually). 
## Values to Consider
When creating this dashboard, I wanted to make sure of three things:
1. My family would be safe (Violent Crime Rate)
2. My children would be well educated (School Score by State)
3. My family would not be stressed about money (Money Leftover After Expenses)
## Data
### Methodology
VCR by State was simple enough to put into a table after data was gathered from ![CSG Justice Center](https://projects.csgjusticecenter.org/tools-for-states-to-address-crime/50-state-crime-data/).

<details>
<summary>VCR by State</summary>

TLDR: Maine and New Hampshire tie for the safest at 100.1 per 100,000 people. Alaska as the most dangerous at 724.1 per 100,000 people. National average is 327.6.

| State | VCR |
|---|---|
| Alabama | 359.9 |
| Alaska | 724.1 |
| Arizona | 421.9 |
| Arkansas | 579.4 |
| California | 486 |
| Colorado | 476.3 |
| Connecticut | 136 |
| Delaware | 360.8 |
| Florida | 267.1 |
| Georgia | 325.7 |
| Hawaii | 217.7 |
| Idaho | 230.6 |
| Illinois | 289.2 |
| Indiana | 312.9 |
| Iowa | 243.3 |
| Kansas | 438.7 |
| Kentucky | 213.1 |
| Louisiana | 519.8 |
| Maine | 100.1 |
| Maryland | 420.4 |
| Massachusetts | 314.7 |
| Michigan | 434.3 |
| Minnesota | 256.6 |
| Mississippi | 210.5 |
| Missouri | 462 |
| Montana | 423.5 |
| National | 327.6 |
| Nebraska | 220.5 |
| Nevada | 402 |
| New Hampshire | 110.1 |
| New Jersey | 217.7 |
| New Mexico | 717.1 |
| New York | 380.2 |
| North Carolina | 375.8 |
| North Dakota | 254.3 |
| Ohio | 293.7 |
| Oklahoma | 422.8 |
| Oregon | 331 |
| Pennsylvania | 245.6 |
| Rhode Island | 153.6 |
| South Carolina | 436.7 |
| South Dakota | 362.3 |
| Tennessee | 592.3 |
| Texas | 389.4 |
| Utah | 229.6 |
| Vermont | 219.1 |
| Virginia | 217.9 |
| Washington | 326.1 |
| West Virginia | 248.8 |
| Wisconsin | 278.5 |
| Wyoming | 203.4 |

</details>


The School Score had to be calculated by scanning the ![National Report Card website.](https://www.nationsreportcard.gov/profiles/stateprofile?sfj=NP&chort=1&sub=MAT&sj=&st=MN&year=2024R3) A limitation was that the 2024 data only covers reading and math up to 8th grade. 
The data was summed and averaged in the following way:
Subject Score = (grade 8 score + grade 4 score)/2
School Score = (subject score a + subject score b)/2

<details>
<summary>School Score by State</summary>
  
TLDR: Massachusetts had the highest score at 255.5 and New Mexico had the lowest score at 231.5. National average is 246.

| State | Score |
|---|---|
| Alabama | 240.25 |
| Alaska | 234.5 |
| Arizona | 241 |
| Arkansas | 240.25 |
| California | 242 |
| Colorado | 250.75 |
| Connecticut | 249.5 |
| Delaware | 238.75 |
| Florida | 245.25 |
| Georgia | 244.5 |
| Hawaii | 245.5 |
| Idaho | 248.25 |
| Illinois | 247.25 |
| Indiana | 250 |
| Iowa | 247 |
| Kansas | 244.75 |
| Kentucky | 246.25 |
| Louisiana | 243.75 |
| Maine | 242.75 |
| Maryland | 244 |
| Massachusetts | 255.5 |
| Michigan | 242.25 |
| Minnesota | 249.25 |
| Mississippi | 245 |
| Missouri | 243 |
| Montana | 248.75 |
| National | 246 |
| Nebraska | 246.5 |
| Nevada | 241 |
| New Hampshire | 251.75 |
| New Jersey | 252.5 |
| New Mexico | 231.5 |
| New York | 244.25 |
| North Carolina | 245.75 |
| North Dakota | 248.5 |
| Ohio | 248.5 |
| Oklahoma | 238.25 |
| Oregon | 239.75 |
| Pennsylvania | 247.25 |
| Rhode Island | 245.25 |
| South Carolina | 243.75 |
| South Dakota | 248.75 |
| Tennessee | 247.5 |
| Texas | 243.5 |
| Utah | 251 |
| Vermont | 245.25 |
| Virginia | 245.75 |
| Washington | 246.75 |
| West Virginia | 236.5 |
| Wisconsin | 249.25 |
| Wyoming | 250.75 |
</details>

### Sources

## Findings

## Requirements

## How to Run Locally
