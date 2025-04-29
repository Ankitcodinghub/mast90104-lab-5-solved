# mast90104-lab-5-solved
**TO GET THIS SOLUTION VISIT:** [MAST90104 Lab 5 Solved](https://www.ankitcodinghub.com/product/mast90104-mast09104-a-first-course-in-statistical-learning-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;112913&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;MAST90104 Lab 5 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Note that some of these involve R.

1. The following questions are about leverage

(a) Suppose that H is an idempotent and symmetric matrix. Show that the diagonal entries of H are in [0,1] and that their sum is the rank of H.

(b) Interpret part (a) in terms of leverage.

(c) The formula for the variance of the ith residual is var (ε) = σ2(1 − Hii). If observation i has a leverage close to 1, how does this show that the response variable, y, for a row of the X matrix with large leverage can have a significant effect on the model parameters? When does such an observation have a significant effect?

2. For simple linear regression, y = β0 +β1x+ε, show that a 100(1−α)% confidence interval for the mean response when x = x∗ can be written as

where .

Similarly, show that a 100(1 − α)% prediction interval for a new response when x = x∗ can be written as

.

3. We can generate some data for a simple linear regression as follows:

n &lt;- 30 x &lt;- 1:n y &lt;- x + rnorm(n)

Construct 95% CI’s for Ey and 95% PI’s for y, when x = 1,2,…,n. Join them up and plot them on a graph of y against x. Your plot should look something like this:

What proportion of the y’s should you expect to lie beyond the outer lines?

4. In this exercise, we look at the dangers of overfitting. Generate some observations from a simple linear regression:

set.seed(3) X &lt;- cbind(rep(1,100), 1:100) beta &lt;- c(0, 1) y &lt;- X %*% beta + rnorm(100)

Put aside some of the data for testing and some for fitting:

Xfit &lt;- X[1:50,] yfit &lt;- y[1:50] Xtest &lt;- X[51:100,] ytest &lt;- y[51:100]

x

(a) Using only the fitting data, estimate β and hence the residual sum of squares. Also calculate the residual sum of squares for the test data, that is, .

Now add 10 extra predictor variables which we know have nothing to do with the response:

X &lt;- cbind(X, matrix(runif(1000), 100, 10))

Xtest &lt;- X[51:100,]

Xfit &lt;- X[1:50,]

Again using only the fitting data, fit the linear model y = Xβ+ε, and show that the residual sum of squares has reduced (this has to happen). Then show that the residual sum of squares for the test data has gone up (this happens most of the time).

Explain what is going on.

(b) Repeat the above, but this time add x2, x3 and x4 terms:

X &lt;- cbind(X[, 1:2], (1:100)^2, (1:100)^3, (1:100)^4)

Lab questions

1. What will be the output of the following code? Try to answer this without typing it up.

fb &lt;- function(n) {

if (n == 1 || n == 2) {

return(1)

} else { return(fb(n – 1) + fb(n – 2))

}

} fb(8)

2. Let be a square matrix, and denote by A(−i,−j) the matrix with row i and column j removed. If A is a 1×1 matrix then det(A), the determinant of A, is just a1,1. For n×n matrices we have, for any i,

n det(A) = X(−1)i+j ai,j det(A(−i,−j)).

j=1

Use this to write a recursive function to calculate det(A).

3. This question writes a function to calculate leverages and generate histograms for them, and applies it to three different datasets in order to better understand leverage.

(a) In R, generate 20 observations from a standard bivariate normal distribution with correlation 0.7. (You can do this using the definition and pairs of standard independent normal random variables or using the function rmvnorm in the package mvtnorm). The three data sets are pairs (x1,y1),(x2,y2),(x3,y3) with the first data set having 20 pairs of (x,y) and the second two having 21. Specifically, the three data sets are:

i. The 20 bivariate observations, labelling the first of each pair as x1 in R, and the second as y1.

ii. New variables, x2, y2, which include the pairs (x1,y1) together with an additional point (10,10). iii. New variables, x3, y3, which include pairs in (x1,y1) together with an additional point (10,−0.3).

(b) Fit simple linear regression models of the response yto the predictor x for each of the three data sets in part (a), storing the results in model1, model2, model3, including the options x=TRUE in order that it is possible to access the X matrix of the models subsequently.

i. writeLines

ii. noquote to get text strings without quotes printed out

iii. paste including the text string ” n” to get a new line before a subsequent print

(d) Generate the printouts of leverages and histogram of leverages for the three models.

(e) Plot the data in y1 versus x1 using the options xlim and ylim to make sure that the axes go from -2.1 to 11. Add the point (10,10) with an upper triangle and point (10,−0.3) with a lower triangle. Add the lines from model2 and model3 using dashed and dotted lines. Add the line from model1 in a solid line using the intercept and slope inputs.
