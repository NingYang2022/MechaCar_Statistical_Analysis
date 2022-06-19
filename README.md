
# MechaCar Statistical Analysis

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


