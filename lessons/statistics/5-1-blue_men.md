[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

My solution is the following: 

```python
import brfss
import scipy.stats

df = brfss.ReadBrfss()
df_m = df[df.sex == 1]
heights = df_m.htm3

model_distribution_normal = scipy.stats.norm(loc=178, scale=7.7)

lower_hight_cm = (5 + 10 * 0.0833333) * 30.48
upper_hight_cm = (6 + 1 * 0.0833333) * 30.48
    
p_top = model_distribution_normal.cdf(upper_hight_cm)    
p_bottom = model_distribution_normal.cdf(lower_hight_cm)  

p_top-p_bottom
```

My answer is the following:

**0.34274733076244224**
