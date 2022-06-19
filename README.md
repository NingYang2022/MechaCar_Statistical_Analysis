
# MechaCar Statistical Analysis

## <font color=#6495ED>Background:</font>
AutosRUs’ newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team’s progress. AutosRUs’ upper management has called on us to review the production data for insights that may help the manufacturing team.

In this challenge, we will do the following:
* Perform multiple linear regression analysis to identify which variables in the dataset predict the mpg of MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots
* Run t-tests to determine if the manufacturing lots are statistically different from the mean population
* Design a statistical study to compare vehicle performance of the MechaCar vehicles against vehicles from other manufacturers. For each statistical analysis, you’ll write a summary interpretation of the findings.

## <font color=#6495ED>Data Resource:</font>
*  MechaCar MPG dataset
*  Suspension Coil dataset

## <font color=#6495ED>Software:</font>
R-Base 3.6.3, RStudio 1.3.1

## <font color=#6495ED>Linear Regression to Predict MPG</font>
!["Deliverable_1_lm"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_1_lm.png?raw=true)

!["Deliverable_1_summary"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_1_summary.png?raw=true)

### <font color=#6495D>Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?</font>

The **Vehicle Length** and **Ground Clearence** had a non-random amount of variance to the mpg values.

In the summary output, each Pr(>|t|) value represents the probability that each coefficient contributes a random amount of variance to the linear model. According to our results, ```Vehicle Length: 5.08e-08``` and ```Ground Clearence: 5.21e-08``` (as well as ```intercept: 5.08e-08```) are statistically unlikely to provide random amounts of variance to the linear model. In other words the **Vehicle Length** and **Ground Clearence** have a significant impact on mpg values.

### <font color=#6495D>Is the slope of the linear model considered to be zero? Why or why not?</font>

The slope of the linear model is **not** considered to be zero because the p-value is less than 0.05.

```p-Value: 5.35e-11```, is much smaller than significance level of 0.05 which indicates there is sufficient evidence to **reject our null hypothesis**, which means the slope of this linear model is **not zero**.


### <font color=#6495D>Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?</font>
This linear model predict mpg of MechaCar prototypes **effectively**.

```Multiple R-squared: 0.7149```means that 71.49% of mpg predictions will be determined by the model. In addition, ```p-Value: 5.35e-11``` is smaller than the desired significance level of 0.05. These indicate this multiple regression model predict mpg **effectively**.

## <font color=#6495ED>Summary Statistics on Suspension Coils</font>

Total summary dataframe:

!["Deliverable_2_total_summary.png"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_2_total_summary.png?raw=true)

Lot summary dataframe:

!["Deliverable_2_lot_summary.png"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_2_lot_summary.png?raw=true)

### <font color=#6495D>The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?</font>

* The **total** summary result shows ```Var_Total: 62.29356``` meets the variance of the suspension coils must not exceed 100 PSI.

* **Lot 1**(```Var_by_lot: 0.9795918```) and **Lot 2**(```Var_by_lot: 7.4693878```) are well within the 100 PSI variance requirement. However, **Lot 3**(```Var_by_lot: 170.2861224```) does not predict to design specifications because variance is greater than 100 PSI.

## <font color=#6495ED> T-Tests on Suspension Coils</font>

Suspension Table T-Test:

!["Deliverable_3_01"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_3_01.png?raw=true)

The **true mean of the sample is 1498.78**.  the **p-Value is 0.06**, which is greater than the  significance level of 0.05, there is **NOT enough evidence to reject the null hypothesis**. That indicates the mean of all  manufacturing lots is **not** statistically **different** from the presumed population mean of 1500.


Lot 1 T-Test:

!["Deliverable_3_lot1.png"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_3_lot1.png?raw=true)

The **true mean of the sample is 1500**.  the **p-Value is 1**, which is greater than the  significance level of 0.05, there is **NOT enough evidence to reject the null hypothesis**. That indicates the mean of   manufacturing lot1 is statistically **similar** to the presumed population mean of 1500.


Lot 2 T-Test:

!["Deliverable_3_lot2.png"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_3_lot2.png?raw=true)

The **true mean of the sample is 1500.02**.  the **p-Value is 0.61**, which is greater than the  significance level of 0.05, there is **NOT enough evidence to reject the null hypothesis**. That indicates the mean of  manufacturing lot2 is statistically **similar** to the presumed population mean of 1500.


Lot 3 T-Test:

!["Deliverable_3_lot3.png"](https://github.com/NingYang2022/MechaCar_Statistical_Analysis/blob/main/images/Deliverable_3_lot3.png?raw=true)

The **true mean of the sample is 1496.14**.  the **p-Value is 0.04**, which is smaller than the  significance level of 0.05, there is **enough evidence to reject the null hypothesis**. That indicates the mean of  manufacturing lot3 is statistically **different** from the presumed population mean of 1500.


## <font color=#6495ED> Study Design: MechaCar vs Competition:</font>

There are many factors that would have impact on the sales. The statistical study would compare some metrics of MechaCar against competitors to determine if there is a correlation to higher sales then others.
### <font color=#6495D> Metrics to test</font>
* **Sales** (Dependent)
* **Brand popularity** (Independent)
* **Cost** (Independent)
* **Maintenance cost** (Independent)
* **Highway fuel efficiency** (Independent)
* **Safety rating** (Independent)


### <font color=#6495D> Null and Alternate Hypothesis:</font>

**Null Hypothesis(H<sub>0</sub>)**: MechaCar would have higher sales based on its performance of key metrics against competitors.

**Alternative Hypothesis(H<sub>a</sub>)**:MechaCar would not have higher sales based on its performance of key metrics against competitors.
### <font color=#6495D> Statistical Test</font>

A **multiple linear regression** would be used to determine the factors that have the highest correlation with sales; what factor or combination of factors has the greatest impact on the sales.

### <font color=#6495D> Data needed</font>
We would need to collect the metric data for comparable models of MechaCar and main competitors for the past 5 years.
