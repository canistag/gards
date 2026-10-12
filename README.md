# GARDS: A Family Planning Visualization Dashboard

> ### Gards
> 
> Language: Gothic
> 
> Part of speech: noun
> 
> 1. house; 2. family; household; 3. yard

A dashboard that visualizes the cost of supporting a family across all fifty states of the US. 

![Family](https://github.com/canistag/gards/blob/main/family%20visualizer.png) 

## Question: Where is the most cost effective place to have a family?

States that met the criteria: Kentucky, Iowa, North Dakota, Ohio, Nebraska, Indiana, Illinois, Wyoming, Wisconsin, Pennsylvania. Have a kid or two here!

The states that were deemed the most cost effective places to raise a family were considered areas that met these conditions:

- Below the national average in crime (327.6)
- Above the national average for school score (246)
- Below the national average for expenses (83661.64)

# Question: What are the most and least expensive places to have a family that meet the national criteria?

If you have a lot of money, Massachusetts. If you don't, Kentucky.

## Assumptions
An assumption I have made is that the average family consists of two parents, two children, a dog, and a cat. In addition to this, each family will have a 3 bedroom 2 bathroom house, and a 401k fund for each parent. For the children, each will have a Roth IRA savings account, and a 529 college savings account. Each of these funds and or savings accounts will be a recurring expense of $100 each per month ($1200 annually). 

## Values to Consider
When creating this dashboard, I wanted to make sure of three things:
1. My family would be safe (Violent Crime Rate)
2. My children would be well educated (School Score by State)
3. My family would not be stressed about money (Money Leftover After Expenses)


## Data
### Methodology
VCR by State was simple enough to put into a table after data was gathered from ![CSG Justice Center](https://projects.csgjusticecenter.org/tools-for-states-to-address-crime/50-state-crime-data/).

<details>
<summary>Table</summary>

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
<summary>Table</summary>
  
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

The most time consuming and variable value was most likely cost of living. In order to properly gauge the cost, multiple values had to be summed:

- Average Cost to Raise a Child per State x 2
  TLDR: Massachusetts is the highest at 44k, Mississippi is the lowest at 19k. National is 27K.
  <details>
    <summary>Table</summary>
  
  | State | Cost to Raise a Child |
  |---|---|
  | Alabama | $20,550 |
  | Alaska | $32,947 |
  | Arizona | $26,624 |
  | Arkansas | $21,840 |
  | California | $35,651 |
  | Colorado | $34,986 |
  | Connecticut | $41,808 |
  | Delaware | $24,544 |
  | Florida | $24,045 |
  | Georgia | $21,299 |
  | Hawaii | $33,363 |
  | Idaho | $24,378 |
  | Illinois | $27,206 |
  | Indiana | $27,914 |
  | Iowa | $22,173 |
  | Kansas | $21,757 |
  | Kentucky | $20,758 |
  | Louisiana | $21,798 |
  | Maine | $28,912 |
  | Maryland | $31,283 |
  | Massachusetts | $44,221 |
  | Michigan | $23,587 |
  | Minnesota | $33,197 |
  | Mississippi | $19,178 |
  | Missouri | $26,042 |
  | Montana | $28,954 |
  | National | $27,743 |
  | Nebraska | $25,709 |
  | Nevada | $27,123 |
  | New Hampshire | $32,739 |
  | New Jersey | $35,069 |
  | New Mexico | $25,210 |
  | New York | $33,280 |
  | North Carolina | $23,587 |
  | North Dakota | $24,752 |
  | Ohio | $27,706 |
  | Oklahoma | $25,210 |
  | Oregon | $33,114 |
  | Pennsylvania | $31,741 |
  | Rhode Island | $32,614 |
  | South Carolina | $23,296 |
  | South Dakota | $21,174 |
  | Tennessee | $21,424 |
  | Texas | $22,672 |
  | Utah | $26,957 |
  | Vermont | $38,272 |
  | Virginia | $28,330 |
  | Washington | $35,027 |
  | West Virginia | $22,422 |
  | Wisconsin | $27,955 |
  | Wyoming | $22,755 |
  </details>
  
- Average Cost of a Dog + Average Cost of a Cat
  TLDR: Hawaii is the highest for both pets. North Dakota is the cheapest. Dog national is $1,351. Cat national is $1,820. Summed together the national average to have both is $3,171.
  <details>
  <summary>Table</summary>
    
  | State          | Cat / year | Dog / year | Pet Total |
  |----------------|------------|------------|-----------|
  | Alabama        | $1,332     | $1,799     | $3,131    |
  | Alaska         | $1,418     | $1,891     | $3,309    |
  | Arizona        | $1,339     | $1,812     | $3,151    |
  | Arkansas       | $1,308     | $1,773     | $3,081    |
  | California     | $1,418     | $1,891     | $3,309    |
  | Colorado       | $1,356     | $1,826     | $3,182    |
  | Connecticut    | $1,324     | $1,792     | $3,116    |
  | Delaware       | $1,341     | $1,812     | $3,153    |
  | Florida        | $1,356     | $1,827     | $3,183    |
  | Georgia        | $1,352     | $1,820     | $3,172    |
  | Hawaii         | $1,458     | $1,933     | $3,391    |
  | Idaho          | $1,331     | $1,800     | $3,131    |
  | Illinois       | $1,371     | $1,841     | $3,212    |
  | Indiana        | $1,366     | $1,839     | $3,205    |
  | Iowa           | $1,337     | $1,806     | $3,143    |
  | Kansas         | $1,307     | $1,771     | $3,078    |
  | Kentucky       | $1,354     | $1,826     | $3,180    |
  | Louisiana      | $1,310     | $1,775     | $3,085    |
  | Maine          | $1,354     | $1,826     | $3,180    |
  | Maryland       | $1,389     | $1,861     | $3,250    |
  | Massachusetts  | $1,334     | $1,804     | $3,138    |
  | Michigan       | $1,339     | $1,810     | $3,149    |
  | Minnesota      | $1,361     | $1,831     | $3,192    |
  | Mississippi    | $1,329     | $1,795     | $3,124    |
  | Missouri       | $1,327     | $1,793     | $3,120    |
  | Montana        | $1,334     | $1,802     | $3,136    |
  | Nebraska       | $1,330     | $1,797     | $3,127    |
  | Nevada         | $1,336     | $1,805     | $3,141    |
  | New Hampshire  | $1,318     | $1,786     | $3,104    |
  | New Jersey     | $1,408     | $1,882     | $3,290    |
  | New Mexico     | $1,335     | $1,803     | $3,138    |
  | New York       | $1,430     | $1,905     | $3,335    |
  | North Carolina | $1,337     | $1,805     | $3,142    |
  | North Dakota   | $1,303     | $1,766     | $3,069    |
  | Ohio           | $1,306     | $1,769     | $3,075    |
  | Oklahoma       | $1,310     | $1,775     | $3,085    |
  | Oregon         | $1,406     | $1,877     | $3,283    |
  | Pennsylvania   | $1,313     | $1,775     | $3,088    |
  | Rhode Island   | $1,353     | $1,825     | $3,178    |
  | South Carolina | $1,335     | $1,804     | $3,139    |
  | South Dakota   | $1,313     | $1,775     | $3,088    |
  | Tennessee      | $1,327     | $1,792     | $3,119    |
  | Texas          | $1,345     | $1,812     | $3,157    |
  | Utah           | $1,365     | $1,838     | $3,203    |
  | Vermont        | $1,350     | $1,822     | $3,172    |
  | Virginia       | $1,370     | $1,840     | $3,210    |
  | Washington     | $1,338     | $1,807     | $3,145    |
  | West Virginia  | $1,341     | $1,811     | $3,152    |
  | Wisconsin      | $1,427     | $1,902     | $3,329    |
  | Wyoming        | $1,395     | $1,866     | $3,261    |
  | National       | $1,351     | $1,820     | $3,171    |
  
  </details>
  
- Average Groceries, Utilities, and House Payment per State
  <details>
    <summary>Table</summary>

    Lowest cost is Mississippi with 35k, highest cost Hawaii at 89k. National is 44k.
    
  | State          | Total House Price | Monthly Payment | Yearly Payment | Utility / mo | Utility / year | Groceries / year | Total      |
  |----------------|-------------------|-----------------|----------------|--------------|----------------|------------------|------------|
  | Alabama        | 219,236           | 1,211.13        | 14,533.56      | $542         | $6,504         | 16,776.24        | $37,814    |
  | Alaska         | 358,736           | 1,981.77        | 23,781.24      | $647         | $7,764         | 22,074           | $53,619    |
  | Arizona        | 406,944           | 2,248.09        | 26,977.08      | $495         | $5,940         | 17,835.84        | $50,753    |
  | Arkansas       | 223,053           | 1,232.21        | 14,786.52      | $502         | $6,024         | 16,776.24        | $37,587    |
  | California     | 718,104           | 3,967.03        | 47,604.36      | $561         | $6,732         | 19,778.28        | $74,115    |
  | Colorado       | 503,084           | 2,779.19        | 33,350.28      | $488         | $5,856         | 18,189           | $57,395    |
  | Connecticut    | 367,669           | 2,031.12        | 24,373.44      | $554         | $6,648         | 18,542.16        | $49,564    |
  | Delaware       | 328,899           | 1,816.94        | 21,803.28      | $570         | $6,840         | 18,012.36        | $46,656    |
  | Florida        | 387,663           | 2,141.57        | 25,698.84      | $480         | $5,760         | 17,659.2         | $49,118    |
  | Georgia        | 284,809           | 1,573.37        | 18,880.44      | $579         | $6,948         | 16,952.88        | $42,781    |
  | Hawaii         | 886,930           | 4,899.68        | 58,796.16      | $616         | $7,392         | 22,956.96        | $89,145    |
  | Idaho          | 417,658           | 2,307.27        | 27,687.24      | $553         | $6,636         | 17,482.56        | $51,806    |
  | Illinois       | 251,379           | 1,388.70        | 16,664.4       | $457         | $5,484         | 17,659.2         | $39,808    |
  | Indiana        | 223,999           | 1,237.44        | 14,849.28      | $526         | $6,312         | 16,952.88        | $38,114    |
  | Iowa           | 212,119           | 1,171.81        | 14,061.72      | $460         | $5,520         | 17,306.04        | $36,888    |
  | Kansas         | 208,892           | 1,153.98        | 13,847.76      | $506         | $6,072         | 17,306.04        | $37,226    |
  | Kentucky       | 216,986           | 1,198.70        | 14,384.4       | $511         | $6,132         | 16,952.88        | $37,469    |
  | Louisiana      | 203,886           | 1,126.33        | 13,515.96      | $511         | $6,132         | 16,776.24        | $36,424    |
  | Maine          | 395,378           | 2,184.19        | 26,210.28      | $527         | $6,324         | 18,189           | $50,723    |
  | Maryland       | 359,950           | 1,988.48        | 23,861.76      | $561         | $6,732         | 18,189           | $48,783    |
  | Massachusetts  | 560,849           | 3,098.30        | 37,179.6       | $543         | $6,516         | 18,895.32        | $62,591    |
  | Michigan       | 234,430           | 1,295.06        | 15,540.72      | $472         | $5,664         | 17,129.4         | $38,334    |
  | Minnesota      | 312,964           | 1,728.91        | 20,746.92      | $451         | $5,412         | 17,835.84        | $43,995    |
  | Mississippi    | 184,154           | 1,017.32        | 12,207.84      | $517         | $6,204         | 16,776.24        | $35,188    |
  | Missouri       | 237,568           | 1,312.40        | 15,748.8       | $631         | $7,572         | 17,129.4         | $40,450    |
  | Montana        | 462,337           | 2,554.09        | 30,649.08      | $503         | $6,036         | 17,482.56        | $54,168    |
  | National       | 325,051           | 1,795.68        | 21,548.16      | $594         | $7,128         | 16,074.24        | $44,750    |
  | Nebraska       | 251,933           | 1,391.76        | 16,701.12      | $484         | $5,808         | 17,306.04        | $39,815    |
  | Nevada         | 405,484           | 2,240.02        | 26,880.24      | $430         | $5,160         | 18,012.36        | $50,053    |
  | New Hampshire  | 463,093           | 2,558.27        | 30,699.24      | $525         | $6,300         | 18,189           | $55,188    |
  | New Jersey     | 472,215           | 2,608.66        | 31,303.92      | $613         | $7,356         | 18,365.52        | $57,025    |
  | New Mexico     | 306,366           | 1,692.46        | 20,309.52      | $384         | $4,608         | 16,952.88        | $41,870    |
  | New York       | 318,382           | 1,758.84        | 21,106.08      | $535         | $6,420         | 18,012.36        | $45,538    |
  | North Carolina | 304,948           | 1,684.63        | 20,215.56      | $493         | $5,916         | 16,952.88        | $43,084    |
  | North Dakota   | 246,697           | 1,362.83        | 16,353.96      | $443         | $5,316         | 17,306.04        | $38,976    |
  | Ohio           | 204,988           | 1,132.42        | 13,589.04      | $590         | $7,080         | 16,952.88        | $37,622    |
  | Oklahoma       | 197,204           | 1,089.42        | 13,073.04      | $522         | $6,264         | 16,776.24        | $36,113    |
  | Oregon         | 467,854           | 2,584.57        | 31,014.84      | $628         | $7,536         | 18,365.52        | $56,916    |
  | Pennsylvania   | 246,367           | 1,361.01        | 16,332.12      | $514         | $6,168         | 17,659.2         | $40,159    |
  | Rhode Island   | 432,623           | 2,389.94        | 28,679.28      | $561         | $6,732         | 18,189           | $53,600    |
  | South Carolina | 283,156           | 1,564.24        | 18,770.88      | $494         | $5,928         | 16,776.24        | $41,475    |
  | South Dakota   | 282,594           | 1,561.14        | 18,733.68      | $428         | $5,136         | 17,306.04        | $41,176    |
  | Tennessee      | 312,147           | 1,724.40        | 20,692.8       | $540         | $6,480         | 16,952.88        | $44,126    |
  | Texas          | 275,076           | 1,519.61        | 18,235.32      | $573         | $6,876         | 17,129.4         | $42,241    |
  | Utah           | 459,879           | 2,540.51        | 30,486.12      | $536         | $6,432         | 17,482.56        | $54,401    |
  | Vermont        | 403,775           | 2,230.58        | 26,766.96      | $483         | $5,796         | 18,542.16        | $51,105    |
  | Virginia       | 330,658           | 1,826.66        | 21,919.92      | $557         | $6,684         | 17,835.84        | $46,440    |
  | Washington     | 544,501           | 3,007.99        | 36,095.88      | $570         | $6,840         | 19,071.96        | $62,008    |
  | West Virginia  | 163,380           | 902.56          | 10,830.72      | $715         | $8,580         | 16,776.24        | $36,187    |
  | Wisconsin      | 287,687           | 1,589.27        | 19,071.24      | $418         | $5,016         | 17,129.4         | $41,217    |
  | Wyoming        | 327,513           | 1,809.28        | 21,711.36      | $575         | $6,900         | 17,482.56        | $46,094    |
  
  </details>
  
  

### Sources
- [Cost to Raise a Child](https://smartasset.com/data-studies/cost-raise-child-state-2025)
- [Cost of 3 Bedroom House](https://finance.yahoo.com/news/cost-own-3-bedroom-home-221034952.html?guccounter=1)
- [Pet Cost](https://petcostplanner.com/cost-by-state/)
- [Grocery Cost](https://grocerymentor.com/budget/grocery-cost-by-state-calculator/)
- [Utility Cost](https://www.move.org/utility-bills-101/#Ranking_table)
- [Mortgage Calculator](https://www.calculator.net/mortgage-calculator.html?chouseprice=327%2C513&cdownpayment=20&cdownpaymentunit=p&cloanterm=30&cinterestrate=7.373&cstartmonth=9&cstartyear=2026&cpropertytaxes=1.2&cpropertytaxesunit=p&chomeins=1%2C500&chomeinsunit=d&cpmi=0&cpmiunit=d&choa=0&choaunit=d&cothercost=4%2C000&cothercostunit=d&cmop=0&cptinc=0&chiinc=0&choainc=0&cocinc=0&cexma=0&cexmsm=9&cexmsy=2026&cexya=0&cexysm=9&cexysy=2026&cexoa=0&cexosm=9&cexosy=2026&caot=0&xa1=0&xm1=9&xy1=2026&xa2=0&xm2=9&xy2=2026&xa3=0&xm3=9&xy3=2026&xa4=0&xm4=9&xy4=2026&xa5=0&xm5=9&xy5=2026&xa6=0&xm6=9&xy6=2026&xa7=0&xm7=9&xy7=2026&xa8=0&xm8=9&xy8=2026&xa9=0&xm9=9&xy9=2026&xa10=0&xm10=9&xy10=2026&csbw=1&printit=0&x=Calculate)
