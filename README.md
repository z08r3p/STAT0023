java c
STAT0023 23-24: Question 9 
Introduction 
Consider using data (x ,y ), … (x ,y ) to estimate the regression function f(•) in the regression model Y = f(x ) + ε (i=1, …, n), where the {ε } are independent N(0,σ ) random variables. No assumptions are made about the function f(•) except that it is differentiable. Local linear regression is a nonparametric approach for estimating f(•). For a specific value x , the local linear regression estimate of f(x ) is obtained as the fitted value from a weighted least-squares regression of the {y } upon the {x }: specifically, it is the value of β obtained by minimising the expression

where the {w } are weights (see below). In this case, it can be shown that the required estimate of f(x ) is

where  The weights {w } are chosen so that observations with values close to x have a high weight and observations further away have near-zero weight: this ensures that the estimate is primarily based on observations with x values in the neighbourhood of x , hence the term 'local' linear regression. To construct the weights it is common to use the probability density function (pdf) of a normal distribution with mean 0 and standard deviation h for some user-specified value of h, so that  where is the pdf of a standard normal distribution.
As described above, the local linear regression technique will provide an estimate of the single value f(x ). To obtain an est代 写STAT0023 23-24: Question 9R
代做程序编程语言imate of the entire regression function f(•) over some range (x , x ), it is necessary to set up a grid of values of x covering this range and to estimate the value of f(•) for each of these values: if the grid is fine enough, the estimates can then be plotted against the x values to obtain a smooth curve. Note: when doing this, the weights {w } will be different for each grid node - as will the quantities A, B and C.
Your task 
Write an R function called llr(), to carry out a local linear regression estimate of y upon x as described above. The arguments to your function should be: y, a vector containing the {y }; x, a vector containing the {x }; xlims, a vector of length 2 containing the values of x and x (see above); n.grid, the number of points required in the grid of values of x ; and h, the standard deviation of the normal distribution used to calculate the weights {w }. The default value of n.grid should be 100, and the default value of h should be (x - x ) / 4. Your function should return a list containing components x and y (vectors containing the original data values); x0.grid (a vector containing the grid of values of x in increasing order) and f.hat (a vector containing the corresponding vector of estimates ). In writing your function, you may not use any existing R routines for local regression.















         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
