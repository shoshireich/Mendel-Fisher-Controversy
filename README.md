# Mendel-Fisher-Controversy
## Abstract
Mendel is widely known as the founder of scientific field of genetics for his many pea-plant experiments in the mid 19th century. In the early 20th century, British statistician and geneticist Ronald Fisher analyzed Mendel's work and concluded that a chi-squared analysis shows that Mendel's results are too perfect; Mendel's experimental data fits too well to theory expectations, suggesting Mendel may have (intentionally or not) altered his data. Fisher came to this conclusion through theoretical analyses. The task here is to evaluate the legitimacy of Fisher's claims using an empirical approach. The results from simulating all of Mendel's 84 experiments suggests that Mendel may have indeed falsified his data. Isolating the 69 experiments that do not involve an expected ratio of 0.6291:0.3709 also indicates that Mendel may have removed extreme values from his data. One of Mendel's experiments yielded results that had such a large deviation from the expectation that Mendel was compelled to repeat this experiment. However, an empirical analysis of observed results for this experiment indicates that Mendel's deviation was not large enough to be cause for concern. 

## Methods
First, I look at all 84 of Mendel's experiments. The χ2 statistic for each of Mendel's 84 experiments is calculated, along with the sum of these values (χ2_84 statistic). Then each of Mendel's experiments are simulated 500 times. This number of simulations was chosen because this is when the χ2 statistic plateaus. For each simulation, the χ2 statistic is calculated for each experiment. The χ2 statistics for Mendel's data are then compared to the distribution of the results from the simulations. This process is repeated for the χ2_84 statistic.

Looking at the 69 experiments that do not involve an expected ratio of 0.6291:0.3709, a similar approach is done in order to evaluate the legitimacy of the claim that Mendel may have removed extreme values. The χ statistic (√χ2) is calculated from Mendel's data and compared to the distribution of χ statistics for each of the 69 experiments across 500 simulations. 

Lastly, I examine the one experiment that Mendel chose to repeat. As above, a distribution of χ statistics is created by simulating the experiment 500 times. This distribution is used to determine the likelihood of seeing results that Mendel reached in each of his two trials. 

## Results and Discussion
As shown in Figure 1, the probability of observing a  χ2_84 statistic less than that from Mendel's data is less than 1%. This is not within the 5% confidence interval for the null hypothesis that Mendel did not falsify his data. Therefore, we reject the null hypothesis, suggesting that Mendel may have falsified his data.
<img src="https://github.com/shoshireich/Mendel-Fisher-Controversy/blob/master/Figures/Figure1.png" width="85%">  
  
When investigating the χ values across the 69 experiments that do not involve the expected 0.6291:0.3709 ratio, the probability of χ values between Mendel's results and the simulated results and are very similar for the mid-ranges (0.25 < P(X) < 0.75). However, Mendel's data deviates from the simulations at the tails (P(X) < 0.25, P(X) > 0.75). This suggests that Mendel may have curated his data and removed extreme values to better fit expectations.
<img src="https://github.com/shoshireich/Mendel-Fisher-Controversy/blob/master/Figures/Figure2.png" width="85%">  

One of the most notable points in Mendel’s original paper is that at one point an experiment yielded 60 heterozygous plants for pod color and 40 were homozygous green, when an expected ratio was 2:1. This departure from expectation was so large that Mendel repeated this experiment recording 65:35 in the subsequent trial. This was the only experiment that Mendel felt compelled to repeat, but should he have been concerned? After simulating the experiment 500 times, Figure 3 shows the distribution of observed ratios. The data from Mendel's first trial deviated from the expected value of 66.6 by 6.67 plants. The probability of observing a deviation greater than or equal to 6.67 is 13.83%. Assuming a 5% likelihood of being generated by the null hypothesis, the maximum allowable deviation to accept is 9.5 plants. Since Mendel's deviation is less than the maximum allowable deviation, Mendel had no reason to be concerned. 
<img src="https://github.com/shoshireich/Mendel-Fisher-Controversy/blob/master/Figures/Figure3.png" width="85%">  
