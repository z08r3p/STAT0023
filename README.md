java c
STAT0023 23-24: Question 13
Introduction 
A contingency table (also called a two-way table) is a way of visualising two categorical variables. For example, suppose we have two categorical variables in a clinical study: treatment (none, placebo, drug) and illness (yes or no) and conduct a study where individuals are randomly assigned into treatment groups. We can then record the outcome of the study in a two-way table:

Mathematically, we can represent such an m × n (here m = 3 and n = 2) table of counts as a matrix of counts X and use the notation  to represent the sum of row i,  the sum of column j, and  the total count of the table.
Now suppose we would like to know whether the treatment affects the probability of illness. In other words, we want to test whether the distribution of each row is the same. In order to do so, we first build the expected cell counts under the null hypothesis that the probability of each column (denoted p1 and p2) is the same for all rows and equal to the overall observed proportion  and  and in general 
In our earlier example,  and  Under this null hypothesis, the expected number of individuals in cell (i, j), denoted eij, is given by 
The dev代 写STAT0023 23-24: Question 13R
代做程序编程语言iation of the observed counts X from the expected counts can then be quantified by computing the test-statistic 
which, under the assumption of the null hypothesis, follows a  distribution with (m - 1)(n - 1) degrees of freedom in large enough samples. A common criterion is to apply this test only if all expected cell counts are at least 5, otherwise this test cannot be used.
Your task 
Write an R function called cont.homo.test to perform. a hypothesis test of homogeneity for an m × n contingency table of counts. The arguments to your function should be: x, a matrix representing a table of counts. Your function should issue an R warning message if any of the expected frequencies are less than 5. Otherwise, your function should return a list containing components expected, the m   × n matrix of expected counts; statistic, the value of the test statistic; p.value, the -value for that test statistic; df, the degrees of freedom of the corresponding  distribution. You may not use any existing R routines for goodness-of-fit testing. Note: the above example is for illustration only, your code needs to work for any table of counts with m, n > 1.



         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
