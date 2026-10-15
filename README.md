<img src="https://github.com/canistag/gards/blob/main/family%20visualizer.png" align="left" width="100" height="100" style="margin-right: 15px;">

# GARDS: A Family Planning Data Analysis

> ### GARDS
> 
> Language: Gothic
> 
> Part of speech: noun
> 
> 1. house; 2. family; household; 3. yard
>

A study that analyzes the cost of supporting a family across all fifty states of the US.
<br clear="left"/>

## Question: 
Where is the most cost effective place to have a family? What about the most and least expensive states to have a family, given the criteria of good schools, safety, and cost of living? 

## Key Findings:

The states that were deemed the most cost effective places to raise a family were considered areas that met these conditions:

- Below the national average in crime (327.6)
- Above the national average for school score (246)
- Below the national average for expenses ($86,462)
- Above the national average for unemployment (3.85%)

States that met the criteria (Definitely have a kid or two here!):
<img width="1286" height="202" alt="image" src="https://github.com/user-attachments/assets/b0c5938a-f60a-4edc-886f-d144a54fb1e6" />

Overall winner is North Dakota with a composite score of 0.9619969801!
<img width="687" height="387" alt="image" src="https://github.com/user-attachments/assets/0c405bf1-a2f9-4ddd-a387-81cb57c35a7e" />



Individual findings include:
- Maine and New Hampshire tie for the safest at 100.1 per 100,000 people. Alaska as the most dangerous at 724.1 per 100,000 people. National average is 327.6.
- Massachusetts had the highest school score at 255.5 and New Mexico had the lowest score at 231.5. National average is 246.
- Massachusetts is the highest in cost to raise a child at 44k, Mississippi is the lowest at 19k. National is 27K.
- Hawaii is the highest for both pets. North Dakota is the cheapest. Dog national is $1,351. Cat national is $1,820. Summed together the national average to have both is $3,171.
- The lowest groceries, utility, and house payment cost is Mississippi with 35k, highest cost Hawaii at 89k. National is 44k.
- California has the highest unemployment rate at 5.1%. South Dakota has the lowest with 2%.

### Relational Findings
An additional sheet was added to calculate correlation between school score, crime rate, and cost of living.

|         | School | Cost  | Crime |
|---------|--------|-------|-------|
| School  | -      | 0.25  | -0.55 |
| Cost    | 0.25   | -     | -0.15 |
| Crime   | -0.55  | -0.15 | -     |

Our biggest indicator is the inverse effect that school and crime have on eachother at -0.55. Low school score means higher crime rate; high school score means lower crime rates.
Cost appears to have little bearing on crime and school scores, indicating there may be another variable at play. 

## More Below
<details>
  <summary>Click to reveal data and more!</summary>
  
## Assumptions
An assumption I have made is that the average family consists of two parents, a child, a dog, and a cat. In addition to this, each family will have a 3 bedroom 2 bathroom house. For the children, each will have a Roth IRA savings account, and a 529 college savings account. Each of these funds and or savings accounts will be a recurring expense of $200 each per month (totaling to $9600 annually). 

## Values to Consider
When creating this dashboard, I wanted to make sure of three things:
1. My family would be safe (Violent Crime Rate)
2. My children would be well educated (School Score by State)
3. My family would not be stressed about money (Money Leftover After Expenses)

## Data
### Methodology
VCR by State was simple enough to put into a table after data was gathered from [CSG Justice Center](https://projects.csgjusticecenter.org/tools-for-states-to-address-crime/50-state-crime-data/).

The School Score had to be calculated by scanning the [National Report Card website.](https://www.nationsreportcard.gov/profiles/stateprofile?sfj=NP&chort=1&sub=MAT&sj=&st=MN&year=2024R3) A limitation was that the 2024 data only covers reading and math up to 8th grade. 
The data was summed and averaged in the following way:

Subject Score = (grade 8 score + grade 4 score)/2
School Score = (subject score a + subject score b)/2

The most time consuming and variable value was most likely cost of living. In order to properly gauge the cost, multiple values per state had to be summed:

- Average Cost to Raise a Child
- Average Cost of a Dog + Average Cost of a Cat
- Average Groceries, Utilities, and House Payment

## The Z Score
The z-score was calculated with a standard formula of (score-mean)/(standard deviation), inverting the sign on cost and crime so that lower values produce higher scores. Then, when calculating the composite score, I assigned a weight of 0.5 to the school score, 0.4 to the crime score, and 0.1 to the cost of living score. This was done to reflect my own values, and will be able to be adjusted in a coming update.
  =AVERAGE((B5*0.5)+(C5*0.4)+(D5*0.1))

## Sheet Conventions
The national scores were placed in their own sheet to prevent errors in the data visualization tool. Facts_costs was getting crowded, so I opted to keep costs and metrics separate; same with the z-scores. Dim_states was built for ease of viewing and access.

## Sources
Last Updated 10-15-2026
- [CSG Justice Center](https://projects.csgjusticecenter.org/tools-for-states-to-address-crime/50-state-crime-data/)
- [National Report Card](https://www.nationsreportcard.gov/profiles/stateprofile?sfj=NP&chort=1&sub=MAT&sj=&st=MN&year=2024R3)
- [Cost to Raise a Child](https://smartasset.com/data-studies/cost-raise-child-state-2025)
- [Cost of 3 Bedroom House](https://finance.yahoo.com/news/cost-own-3-bedroom-home-221034952.html?guccounter=1)
- [Pet Cost](https://petcostplanner.com/cost-by-state/)
- [Grocery Cost](https://grocerymentor.com/budget/grocery-cost-by-state-calculator/)
- [Utility Cost](https://www.move.org/utility-bills-101/#Ranking_table)
- [Mortgage Calculator](https://www.calculator.net/mortgage-calculator.html?chouseprice=327%2C513&cdownpayment=20&cdownpaymentunit=p&cloanterm=30&cinterestrate=7.373&cstartmonth=9&cstartyear=2026&cpropertytaxes=1.2&cpropertytaxesunit=p&chomeins=1%2C500&chomeinsunit=d&cpmi=0&cpmiunit=d&choa=0&choaunit=d&cothercost=4%2C000&cothercostunit=d&cmop=0&cptinc=0&chiinc=0&choainc=0&cocinc=0&cexma=0&cexmsm=9&cexmsy=2026&cexya=0&cexysm=9&cexysy=2026&cexoa=0&cexosm=9&cexosy=2026&caot=0&xa1=0&xm1=9&xy1=2026&xa2=0&xm2=9&xy2=2026&xa3=0&xm3=9&xy3=2026&xa4=0&xm4=9&xy4=2026&xa5=0&xm5=9&xy5=2026&xa6=0&xm6=9&xy6=2026&xa7=0&xm7=9&xy7=2026&xa8=0&xm8=9&xy8=2026&xa9=0&xm9=9&xy9=2026&xa10=0&xm10=9&xy10=2026&csbw=1&printit=0&x=Calculate)

## Future Ideas
- Correlations between cost, safety, and school score
- Adjustable values
- What regions have the most states that are good for families?

</details>
