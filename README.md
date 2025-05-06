# cs229-problem-set-1-supervised-learning-solved
**TO GET THIS SOLUTION VISIT:** [CS229 Problem Set #1-Supervised Learning Solved](https://www.ankitcodinghub.com/product/cs229-problem-set-1-supervised-learning-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;96206&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;3&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (3 votes)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CS229 Problem Set #1-Supervised Learning Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

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
            5/5 - (3 votes)    </div>
    </div>
<div class="page" title="Page 1">
<div class="layoutArea">
<div class="column">
Notes: (1) These questions require thought, but do not require long answers. Please be as concise as possible. (2) If you have a question about this homework, we encourage you to post your question on our Piazza forum, at http://piazza.com/stanford/fall2018/cs229. (3) If you missed the first lecture or are unfamiliar with the collaboration or honor code policy, please read the policy on Handout #1 (available from the course website) before starting work. (4) For the coding problems, you may not use any libraries except those defined in the provided environment.yml file. In particular, ML-specific libraries such as scikit-learn are not permitted. (5) To account for late days, the due date listed on Gradescope is Oct 20 at 11:59 pm. If you submit after Oct 17, you will begin consuming your late days. If you wish to submit on time, submit before Oct 17 at 11:59 pm.

All students must submit an electronic PDF version of the written questions. We highly recom- mend typesetting your solutions via LATEX. If you are scanning your document by cell phone, please check the Piazza forum for recommended scanning apps and best practices. All students must also submit a zip file of their source code to Gradescope, which should be created using the make zip.py script. In order to pass the auto-grader tests, you should make sure to (1) restrict yourself to only using libraries included in the environment.yml file, and (2) make sure your code runs without errors using the run.py script. Your submission will be evaluated by the auto-grader using a private test set.

</div>
</div>
</div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 2 1. [40 points] Linear Classifiers (logistic regression and GDA)

In this problem, we cover two probabilistic linear classifiers we have covered in class so far. First, a discriminative linear classifier: logistic regression. Second, a generative linear classifier: Gaussian discriminant analysis (GDA). Both the algorithms find a linear decision boundary that separates the data into two classes, but make different assumptions. Our goal in this problem is to get a deeper understanding of the similarities and differences (and, strengths and weaknesses) of these two algorithms.

For this problem, we will consider two datasets, provided in the following files: i. data/ds1_{train,valid}.csv

ii. data/ds2_{train,valid}.csv

Each file contains m examples, one example (x(i),y(i)) per row. In particular, the i-th row

contains columns x(i) ∈ R, x(i) ∈ R, and y(i) ∈ {0,1}. In the subproblems that follow, we 01

will investigate using logistic regression and Gaussian discriminant analysis (GDA) to perform binary classification on these two datasets.

(a) [10 points] In lecture we saw the average empirical loss for logistic regression: 1 􏰈m

J(θ) = −m y(i) log(hθ(x(i))) + (1 − y(i))log(1 − hθ(x(i))), i=1

where y(i) ∈ {0, 1}, hθ(x) = g(θT x) and g(z) = 1/(1 + e−z).

Find the Hessian H of this function, and show that for any vector z, it holds true that

zT Hz ≥ 0.

</div>
</div>
<div class="layoutArea">
<div class="column">
Hint: You may want to start by showing that 􏰁i 􏰁j zixixjzj = (xT z)2 ≥ 0. Recall also

that g′(z) = g(z)(1 − g(z)).

Remark: This is one of the standard ways of showing that the matrix H is positive semi-

definite, written “H ≽ 0.” This implies that J is convex, and has no local minima other

than the global one. If you have some other way of showing H ≽ 0, you’re also welcome to use your method instead of the one above.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 3

(b) [5 points] Coding problem. Follow the instructions in src/p01b logreg.py to train a logistic regression classifier using Newton’s Method. Starting with θ = ⃗0, run Newton’s Method until the updates to θ are small: Specifically, train until the first iteration k such that ∥θk − θk−1∥1 &lt; ǫ, where ǫ = 1 × 10−5. Make sure to write your model’s predictions to the file specified in the code.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 4 (c) [5 points] Recall that in GDA we model the joint distribution of (x,y) by the following

</div>
</div>
<div class="layoutArea">
<div class="column">
equations:

</div>
</div>
<div class="layoutArea">
<div class="column">
p(y) = 􏰆φ ify=1 1−φ ify=0

p(x|y=0) = 1 exp􏰄−1(x−μ0)TΣ−1(x−μ0)􏰅 (2π)n/2|Σ|1/2 2

p(x|y=1) = 1 exp􏰄−1(x−μ1)TΣ−1(x−μ1)􏰅, (2π)n/2|Σ|1/2 2

</div>
</div>
<div class="layoutArea">
<div class="column">
where φ, μ0, μ1, and Σ are the parameters of our model.

Suppose we have already fit φ, μ0, μ1, and Σ, and now want to predict y given a new point

x. To show that GDA results in a classifier that has a linear decision boundary, show the posterior distribution can be written as

p(y = 1 | x;φ,μ0,μ1,Σ) = 1 , 1 + exp(−(θT x + θ0))

where θ ∈ Rn and θ0 ∈ R are appropriate functions of φ, Σ, μ0, and μ1. Answer:

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 5

(d) [7 points] For this part of the problem only, you may assume n (the dimension of x) is 1, so that Σ = [σ2] is just a real number, and likewise the determinant of Σ is given by |Σ| = σ2. Given the dataset, we claim that the maximum likelihood estimates of the parameters are given by

1 􏰈m

φ=m 1{y(i)=1}

</div>
</div>
<div class="layoutArea">
<div class="column">
μ 0 =

μ = 􏰁􏰈

</div>
</div>
<div class="layoutArea">
<div class="column">
i=1

􏰁mi=1 1{y(i) = 0}x(i) 􏰁 􏰁 mi = 1 1 { y ( i ) = 0 }

</div>
</div>
<div class="layoutArea">
<div class="column">
mi=1 1{y(i) = 1}x(i) 1 mi=1 1{y(i) = 1}

</div>
</div>
<div class="layoutArea">
<div class="column">
Σ = m The log-likelihood of the data is

</div>
<div class="column">
i=1

</div>
</div>
<div class="layoutArea">
<div class="column">
1m

</div>
<div class="column">
(x(i) − μy(i) )(x(i) − μy(i) )T

</div>
</div>
<div class="layoutArea">
<div class="column">
m

log 􏰉 p(x(i), y(i); φ, μ0, μ1, Σ)

i=1 m

i=1

</div>
</div>
<div class="layoutArea">
<div class="column">
l(φ, μ0, μ1, Σ) =

= log 􏰉 p(x(i)|y(i); μ0, μ1, Σ)p(y(i); φ).

</div>
</div>
<div class="layoutArea">
<div class="column">
By maximizing l with respect to the four parameters, prove that the maximum likelihood estimates of φ, μ0,μ1, and Σ are indeed as given in the formulas above. (You may assume that there is at least one positive and one negative example, so that the denominators in the definitions of μ0 and μ1 above are non-zero.)

Answer:

</div>
</div>
</div>
<div class="page" title="Page 6">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 6

(e) [3 points] Coding problem. Insrc/p01egda.py, fill in the code to calculate φ, μ0, μ1, and Σ, use these parameters to derive θ, and use the resulting GDA model to make predictions on the validation set.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 7">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 7

(f) [5 points] For Dataset 1, create a plot of the validation set with x1 on the horizontal axis, and x2 on the vertical axis. To visualize the two classes, use a different symbol for examples x(i) with y(i) = 0 than for those with y(i) = 1. On the same figure, plot the decision boundary found by logistic regression in part (b). Make an identical plot with the decision boundary found by GDA in part (e).

Answer:

</div>
</div>
</div>
<div class="page" title="Page 8">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 8

(g) [5 points] Repeat the steps in part (f) for Dataset 2. On which dataset does GDA seem to perform worse than logistic regression? Why might this be the case?

Answer:

</div>
</div>
</div>
<div class="page" title="Page 9">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 9

(h) [3 extra credit points] For the dataset where GDA performed worse in parts (f) and (g), can you find a transformation of the x(i)’s such that GDA performs significantly better? What is this transformation?

Answer:

</div>
</div>
</div>
<div class="page" title="Page 10">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 10 2. [30 points] Incomplete, Positive-Only Labels

In this problem we will consider training binary classifiers in situations where we do not have full access to the labels. In particular, we consider a scenario, which is not too infrequent in real life, where we have labels only for a subset of the positive examples. All the negative examples and the rest of the positive examples are unlabelled.

That is, we assume a dataset {(x(i),t(i),y(i))}mi=1, where t(i) ∈ {0,1} is the “true” label, and

</div>
</div>
<div class="layoutArea">
<div class="column">
where

</div>
<div class="column">
y(i) = 􏰆1 x(i) is labeled 0 otherwise.

</div>
</div>
<div class="layoutArea">
<div class="column">
All labeled examples are positive, which is to say p(t(i) = 1 | y(i) = 1) = 1, but unlabeled examples may be positive or negative. Our goal in the problem is to construct a binary classifier h of the true label t, with only access to the partial labels y. In other words, we want to construct h such that h(x(i)) ≈ p(t(i) = 1 | x(i)) as closely as possible, using only x and y.

Real world example: Suppose we maintain a database of proteins which are involved in transmit- ting signals across membranes. Every example added to the database is involved in a signaling process, but there are many proteins involved in cross-membrane signaling which are missing from the database. It would be useful to train a classifier to identify proteins that should be added to the database. In our notation, each example x(i) corresponds to a protein, y(i) = 1 if the protein is in the database and 0 otherwise, and t(i) = 1 if the protein is involved in a cross-membrane signaling process and thus should be added to the database, and 0 otherwise.

(a) [5 points] Suppose that each y(i) and x(i) are conditionally independent given t(i): p(y(i) =1|t(i) =1,x(i))=p(y(i) =1|t(i) =1).

Note this is equivalent to saying that labeled examples were selected uniformly at random from the set of positive examples. Prove that the probability of an example being labeled differs by a constant factor from the probability of an example being positive. That is, showthatp(t(i) =1|x(i))=p(y(i) =1|x(i))/αforsomeα∈R.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 11">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 11

(b) [5points]Supposewewanttoestimateαusingatrainedclassifierhandaheld-outvalidation set V . Let V+ be the set of labeled (and hence positive) examples in V , given by V+ = {x(i) ∈ V | y(i) = 1}. Assuming that h(x(i)) ≈ p(y(i) = 1 | x(i)) for all examples x(i), show that

h(x(i)) ≈ α for all x(i) ∈ V+.

You may assume that p(t(i) = 1 | x(i)) ≈ 1 when x(i) ∈ V+. Answer:

</div>
</div>
</div>
<div class="page" title="Page 12">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 12 (c) [5 points] Coding problem. The following three problems will deal with a dataset which

we have provided in the following files:

data/ds3_{train,valid,test}.csv

Each file contains the following columns: x1, x2, y, and t. As in Problem 1, there is one example per row.

First we will consider the ideal case, where we have access to the true t-labels for training. In src/p02cde posonly, write a logistic regression classifier that uses x1 and x2 as input features, and train it using the t-labels (you can ignore the y-labels for this part). Output the trained model’s predictions on the test set to the file specified in the code.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 13">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 13

(d) [5 points] Coding problem. We now consider the case where the t-labels are unavail- able, so you only have access to the y-labels at training time. Add to your code in p02cde posonly.py to re-train the classifier (still using x1 and x2 as input features), but using the y-labels only.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 14">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 14 (e) [10 points] Coding problem. Using the validation set, estimate the constant α by aver-

</div>
</div>
<div class="layoutArea">
<div class="column">
aging your classifier’s predictions over all labeled examples in the validation set: α≈ 1 􏰈 h(x(i)).

Add code in src/p02cde posonly.py to rescale your classifier’s predictions from part (d) using the estimated value for α.

Finally, using a threshold of p(t(i) = 1 | x(i)) = 0.5, make three separate plots with the

decision boundaries from parts (c) – (e) plotted on top of the test set. Plot x1 on the horizontal axis and x2 on the vertical axis, and use two different symbols for the positive (t(i) = 1) and negative (t(i) = 0) examples. In each plot, indicate the separating hyperplane with a red line.

Answer:

Remark: We saw that the true probability p(t | x) was only a constant factor away from p(y | x). This means, if our task is to only rank examples (i.e. sort them) in a particular order (e.g, sort the proteins in order of being most likely to be involved in transmitting signals across membranes), then in fact we do not even need to estimate α. The rank based on p(y | x) will agree with the rank based on p(t | x).

</div>
</div>
<div class="layoutArea">
<div class="column">
|V+| x(i)∈V+

</div>
</div>
</div>
<div class="page" title="Page 15">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 15 3. [25 points] Poisson Regression

(a) [5 points] Consider the Poisson distribution parameterized by λ: e−λ λy

p(y;λ)= y! .

Show that the Poisson distribution is in the exponential family, and clearly state the values for b(y), η, T (y), and a(η).

Answer:

</div>
</div>
</div>
<div class="page" title="Page 16">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 16

(b) [3 points] Consider performing regression using a GLM model with a Poisson response variable. What is the canonical response function for the family? (You may use the fact that a Poisson random variable with parameter λ has mean λ.)

Answer:

</div>
</div>
</div>
<div class="page" title="Page 17">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 17

(c) [7 points] For a training set {(x(i),y(i)); i = 1,…,m}, let the log-likelihood of an example be logp(y(i)|x(i);θ). By taking the derivative of the log-likelihood with respect to θj, derive the stochastic gradient ascent update rule for learning using a GLM model with Poisson responses y and the canonical response function.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 18">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 18

(d) [7 points] Coding problem. Consider a website that wants to predict its daily traffic. The website owners have collected a dataset of past traffic to their website, along with some features which they think are useful in predicting the number of visitors per day. The dataset is split into train/valid/test sets and follows the same format as Datasets 1-3:

data/ds4_{train,valid}.csv

We will apply Poisson regression to model the number of visitors per day. Note that ap- plying Poisson regression in particular assumes that the data follows a Poisson distribution whose natural parameter is a linear combination of the input features (i.e., η = θT x). In src/p03d poisson.py, implement Poisson regression for this dataset and use gradient ascent to maximize the log-likelihood of θ.

Answer:

</div>
</div>
</div>
<div class="page" title="Page 19">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 19 4. [15 points] Convexity of Generalized Linear Models

In this question we will explore and show some nice properties of Generalized Linear Models, specifically those related to its use of Exponential Family distributions to model the output.

Most commonly, GLMs are trained by using the negative log-likelihood (NLL) as the loss func- tion. This is mathematically equivalent to Maximum Likelihood Estimation (i.e., maximizing the log-likelihood is equivalent to minimizing the negative log-likelihood). In this problem, our goal is to show that the NLL loss of a GLM is a convex function w.r.t the model parameters. As a reminder, this is convenient because a convex function is one for which any local minimum is also a global minimum.

To recap, an exponential family distribution is one whose probability density can be represented

p(y; η) = b(y) exp(ηT T (y) − a(η)),

where η is the natural parameter of the distribution. Moreover, in a Generalized Linear Model, η is modeled as θT x, where x ∈ Rn are the input features of the example, and θ ∈ Rn are learnable parameters. In order to show that the NLL loss is convex for GLMs, we break down the process into sub-parts, and approach them one at a time. Our approach is to show that the second derivative (i.e., Hessian) of the loss w.r.t the model parameters is Positive Semi-Definite (PSD) at all values of the model parameters. We will also show some nice properties of Exponential Family distributions as intermediate steps.

For the sake of convenience we restrict ourselves to the case where η is a scalar. Assume p(Y|X;θ) ∼ ExponentialFamily(η), where η ∈ R is a scalar, and T(y) = y. This makes the exponential family representation take the form

p(y; η) = b(y) exp(ηy − a(η)).

</div>
</div>
</div>
<div class="page" title="Page 20">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 20 (a) [5 points] Derive an expression for the mean of the distribution. Show that E[Y ; η] = ∂ a(η)

</div>
</div>
<div class="layoutArea">
<div class="column">
∂η (note that E[Y;η] = E[Y | X;η] since η = θTx). In other words, show that the mean of an exponential family distribution is the first derivative of the log-partition function with

</div>
</div>
<div class="layoutArea">
<div class="column">
respect to the natural parameter.

Hint: Start with observing that ∂ 􏰇 p(y; η)dy = 􏰇 ∂ p(y; η)dy. ∂η ∂η

Answer:

</div>
</div>
</div>
<div class="page" title="Page 21">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 21 (b) [5 points] Next, derive an expression for the variance of the distribution. In particular,

show that Var(Y ; η) = ∂2 a(η) (again, note that Var(Y ; η) = Var(Y | X; θ)). In other ∂η

words, show that the variance of an exponential family distribution is the second derivative of the log-partition function w.r.t. the natural parameter.

Hint: Building upon the result in the previous sub-problem can simplify the derivation. Answer:

</div>
</div>
</div>
<div class="page" title="Page 22">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 22

(c) [5 points] Finally, write out the loss function l(θ), the NLL of the distribution, as a function of θ. Then, calculate the Hessian of the loss w.r.t θ, and show that it is always PSD. This concludes the proof that NLL loss of GLM is convex.

Hint 1: Use the chain rule of calculus along with the results of the previous parts to simplify your derivations.

Hint 2: Recall that variance of any probability distribution is non-negative. Answer:

Remark: The main takeaways from this problem are:

• Any GLM model is convex in its model parameters.

• The exponential family of probability distributions are mathematically nice. Whereas cal- culating mean and variance of distributions in general involves integrals (hard), surprisingly we can calculate them using derivatives (easy) for exponential family.

</div>
</div>
</div>
<div class="page" title="Page 23">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 23 5. [25 points] Locally weighted linear regression

(a) [10 points] Consider a linear regression problem in which we want to “weight” different training examples differently. Specifically, suppose we want to minimize

1􏰈m 􏰂 􏰃2 J(θ) = 2 w(i) θT x(i) − y(i) .

i=1

In class, we worked out what happens for the case where all the weights (the w(i)’s) are the

same. In this problem, we will generalize some of those ideas to the weighted setting.

<ol>
<li>[2 points] Show that J(θ) can also be written
J(θ) = (Xθ − y)T W(Xθ − y)

for an appropriate matrix W , and where X and y are as defined in class. Clearly specify

the value of each element of the matrix W .
</li>
<li>[4 points] If all the w(i)’s equal 1, then we saw in class that the normal equation is
XT Xθ = XT y,

and that the value of θ that minimizes J(θ) is given by (XTX)−1XTy. By finding the derivative ∇θJ(θ) and setting that to zero, generalize the normal equation to this weighted setting, and give the new value of θ that minimizes J(θ) in closed form as a function of X, W and y.
</li>
<li>[4 points] Suppose we have a dataset {(x(i), y(i)); i = 1 . . . , m} of m independent ex- amples, but we model the y(i)’s as drawn from conditional distributions with different levels of variance (σ(i))2. Specifically, assume the model
p(y(i)|x(i);θ)= √ 1 exp􏰄−(y(i) −θTx(i))2􏰅 2πσ(i) 2(σ(i) )2

That is, each y(i) is drawn from a Gaussian distribution with mean θT x(i) and variance (σ(i))2 (where the σ(i)’s are fixed, known, constants). Show that finding the maximum likelihood estimate of θ reduces to solving a weighted linear regression problem. State clearly what the w(i)’s are in terms of the σ(i)’s.
</li>
</ol>
Answer:

</div>
</div>
</div>
<div class="page" title="Page 24">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 24 (b) [10 points] Coding problem. We will now consider the following dataset (the formatting

matches that of Datasets 1-4, except x(i) is 1-dimensional): data/ds5_{train,valid,test}.csv

In src/p05b lwr.py, implement locally weighted linear regression using the normal equa- tions you derived in Part (a) and using

w(i) =exp􏰄−∥x(i) −x∥2􏰅. 2τ2

Train your model on the train split using τ = 0.5, then run your model on the valid split and report the mean squared error (MSE). Finally plot your model’s predictions on the validation set (plot the training set with blue ‘x’ markers and the validation set with a red ‘o’ markers). Does the model seem to be under- or overfitting?

Answer:

</div>
</div>
</div>
<div class="page" title="Page 25">
<div class="layoutArea">
<div class="column">
CS229 Problem Set #1 25

(c) [5 points] Coding problem. We will now tune the hyperparameter τ . In src/p05c tau.py, find the MSE value of your model on the validation set for each of the values of τ specified in the code. For each τ, plot your model’s predictions on the validation set in the format described in part (b). Report the value of τ which achieves the lowest MSE on the valid split, and finally report the MSE on the test split using this τ -value.

Answer:

</div>
</div>
</div>
