# QIE-Spring-2018-Research
Quantitative Impact Evaluation semester-long project to investigate Pew Research Center's Cybersecurity Survey pulled from March 30th - May 3rd 2016. Research prompt and specific hypotheses to follow.

---

#Before Log Earn modification, April 6th 
##Earnings amount is skewed

##Code 
---
lm(dfcurrent2$'earn'~dfcurrent2$'economics' + dfcurrent2$political_science + dfcurrent2$'racialasian' + dfcurrent2$'racialblack' + dfcurrent2$'racialpacific' + dfcurrent2$'racialnative' +dfcurrent2$dadbach + dfcurrent2$dadlesshs +dfcurrent2$mombach, + dfcurrent2$momlesshs + dfcurrent2$childliv + dfcurrent2$spowk_full + dfcurrent2$employ_10 + dfcurrent2$employ_25000 + dfcurrent2$citizenusin, + dfcurrent2$minority, + dfcurrent2$bthus + dfcurrent2$gov_inst + dfcurrent2$edu_inst + dfcurrent2$married + dfcurrent2$divorced + dfcurrent2$separated + dfcurrent2$citizendual + dfcurrent2$onedeg +dfcurrent2$twodeg +dfcurrent2$threedeg +dfcurrent2$fourdeg +dfcurrent2$fivedeg +dfcurrent2$gradsupemploy +dfcurrent2$et_priv_prof)
model7<-lm(dfcurrent2$'earn'~dfcurrent2$'economics'+dfcurrent2$'racialasian' + dfcurrent2$'racialblack' + dfcurrent2$'racialpacific' + dfcurrent2$'racialnative' +dfcurrent2$dadbach + dfcurrent2$dadlesshs +dfcurrent2$mombach  + dfcurrent2$momlesshs + dfcurrent2$childliv + dfcurrent2$spowk_full + dfcurrent2$employ_10 +  dfcurrent2$employ_25000 + dfcurrent2$citizenusin + dfcurrent2$minority + dfcurrent2$bthus+ dfcurrent2$gov_inst + dfcurrent2$edu_inst + dfcurrent2$married + dfcurrent2$divorced + dfcurrent2$separated + dfcurrent2$citizendual + dfcurrent2$onedeg  +dfcurrent2$twodeg +dfcurrent2$threedeg +dfcurrent2$fourdeg +dfcurrent2$fivedeg +dfcurrent2$gradsupemploy +dfcurrent2$et_priv_prof)
summary(model7)

##Output
---
Residuals:
    Min      1Q  Median      3Q     Max 
-182961  -40923  -16330    9598 9958931 

Coefficients:
                         Estimate Std. Error t value Pr(>|t|)    
(Intercept)              151794.9   226496.0   0.670 0.502741    
dfcurrent2$economics      37565.3     5518.5   6.807 1.01e-11 ***
dfcurrent2$racialasian    -3319.2     3223.1  -1.030 0.303107    
dfcurrent2$racialblack    -4808.9     4463.9  -1.077 0.281363    
dfcurrent2$racialpacific  -8386.4    10978.2  -0.764 0.444921    
dfcurrent2$racialnative    5749.1     8499.3   0.676 0.498779    
dfcurrent2$dadbach         8805.5     2473.0   3.561 0.000370 ***
dfcurrent2$dadlesshs      10153.0     4337.5   2.341 0.019248 *  
dfcurrent2$mombach          355.9     2476.8   0.144 0.885730    
dfcurrent2$momlesshs       1054.1     4295.5   0.245 0.806157    
dfcurrent2$childliv       11014.9     2452.0   4.492 7.06e-06 ***
dfcurrent2$spowk_full    -23507.2     2424.3  -9.696  < 2e-16 ***
dfcurrent2$employ_10     -15961.9     3960.1  -4.031 5.57e-05 ***
dfcurrent2$employ_25000   15050.6     2626.1   5.731 1.00e-08 ***
dfcurrent2$citizenusin     5918.9     4581.6   1.292 0.196402    
dfcurrent2$minority       -9401.9     3308.4  -2.842 0.004487 ** 
dfcurrent2$bthusY        -12839.5     3759.2  -3.415 0.000637 ***
dfcurrent2$gov_inst      -22896.3     4024.6  -5.689 1.28e-08 ***
dfcurrent2$edu_inst      -40687.0     3454.4 -11.778  < 2e-16 ***
dfcurrent2$married        27992.7     3062.0   9.142  < 2e-16 ***
dfcurrent2$divorced        8378.9     5209.9   1.608 0.107782    
dfcurrent2$separated      -7134.6    11707.9  -0.609 0.542271    
dfcurrent2$citizendual     2794.0     4880.2   0.573 0.566972    
dfcurrent2$onedeg        -74618.9   226453.6  -0.330 0.741771    
dfcurrent2$twodeg        -60158.6   226457.0  -0.266 0.790509    
dfcurrent2$threedeg      -45991.0   226476.0  -0.203 0.839079    
dfcurrent2$fourdeg       -34923.6   226647.9  -0.154 0.877541    
dfcurrent2$fivedeg       -61003.9   229011.6  -0.266 0.789948    
dfcurrent2$gradsupemploy  11249.2     3452.5   3.258 0.001122 ** 
dfcurrent2$et_priv_prof    5636.1     2942.7   1.915 0.055464 .  
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 226400 on 48841 degrees of freedom
  (4223 observations deleted due to missingness)
Multiple R-squared:  0.01793,	Adjusted R-squared:  0.01735 
F-statistic: 30.75 on 29 and 48841 DF,  p-value: < 2.2e-16


###Holding constant race, age, sex, parental education level, children living in the home, employer size, birth region, marital status, and the number of degrees received, economics majors aged 25-55 who work full time make $37,000 more on average than other college graduates, significant at the 1% level.

###Economics majors with a father who completed a bachelor's degree made $8,854 more on average than other economics majors, signficant at the 1% level. Those with a father who did not complete high school made $10,000 more on average than other economics majors, significant at the 10% level. Mother's education level has no statistically significant impact on indiviudls' earnings.  

###Economics majors with children living in the home make $10,904 more on average than other economics majors, statistically significant at the 1% level. Those with spouses who work full time make $23,000 less on average than other economics majors. Those who work in a very small company (less than 10 employees) make $18,000 less than other economics majors, whereas those who work in a very large company (more than 25,000 employees) make $15,606 more than other economics majors, both significant at the 1% level. 

###Minorities make $9,355 less on average than other economics majors, significant at the 5% level; yet those born in the U.S. make $12, 905 less than other economics majors, significant at the 1% level. Those who work for a government or educational instituations make less on average than other majors, significant at the 1% level. Married economics majors make $27,992 more on average than other economics majors, significant at the 1% level.
