Download Link: https://assignmentchef.com/product/solved-rob313-assignment-2-linear-models
<br>



<strong>Q1 </strong>Derive a closed form expression for the weights of the generalized linear model,

), using a least-squares loss and general Tikhonov reg-

ularization. The optimization problem to be solved for the weights can be written as

argmin<em>, </em><strong>w</strong>∈R<em><sup>M</sup></em>

where <strong>Γ </strong>∈ R<em><sup>M</sup></em><sup>×<em>M </em></sup>is a symmetric positive semi-definite matrix whose <em>ij</em>th entry is given by Γ<em><sub>ij</sub>.</em>

<strong>Q2) 3pts </strong>Implement a generalized linear model (GLM) that minimizes the least-squares loss function (using the SVD). By observing the structure of the one-dimensional mauna loa training dataset, design a compact set of basis functions to construct a GLM for this dataset. Justify your design choices. Additionally, choose a regularization parameter <em>λ</em>, and use the validation set to verify your model. Finally, use both the training and validation sets to predict on the test set, plot the prediction relative to the test data, and present the test RMSE. Comment on the performance of your model.

<strong>Q3) 3pts </strong>Considering the same basis functions used in Q2, construct a kernelized GLM from the dual perspective. Select a positive regularization parameter, and construct the model using the Cholesky factorization. Comment on the computational cost and memory requirements of the dual approach versus the primal approach. Also, visualize your designed kernel by plotting <em>k</em>(0<em>,z</em>), and by plotting <em>k</em>(1<em>,z </em>+ 1) where <em>z </em>∈ [−0<em>.</em>1<em>,</em>0<em>.</em>1]. Is your kernel translation-invariant (stationary)? Make your argument based on your plots of the kernel.

<strong>Q4) 4pts </strong>Construct a radial basis function (RBF) model that minimizes the least-squares loss function. Use a Gaussian kernel and consider the grid of shape parameter values <em>θ </em>= {0<em>.</em>05<em>,</em>0<em>.</em>1<em>,</em>0<em>.</em>5<em>,</em>1<em>,</em>2}, consider the grid of regularization parameters {0<em>.</em>001<em>,</em>0<em>.</em>01<em>,</em>0<em>.</em>1<em>,</em>1}, and construct the model using Cholesky factorization. Select the hyperparameters across the grid of possible values by evaluating on the validation set. Construct the model on the datasets iris, rosenbrock (with n train=1000, d=2), and mauna loa. Use both the training and validation sets to predict on the test set, and format your results in a table (present test RMSE for regression datasets, and test accuracy for classification datasets).

<strong>Q5) 5pts </strong>Implement a greedy regression algorithm using a dictionary of Gaussian kernels cen-

tered at the training points. Use the orthogonal matching pursuit metric to select

Page 1 of 2

a new basis function at each iteration. Use the minimum description length (MDL) defined below as a stopping criterion for your greedy algorithm

loss)


where <em>`</em><sub>2</sub>− loss is simply the least-squares training error and <em>k </em>is the iteration number (or number of terms in the greedy model). The MDL metric can be considered to be a surrogate of the generalization error – in other words, this metric will decrease as the model complexity (<em>k</em>) grows and then increase as overfitting starts to occur.

Apply your algorithm to the rosenbrock dataset (with n train=200,d=2) for three different settings of the shape parameter {0<em>.</em>01<em>,</em>0<em>.</em>1<em>,</em>1<em>.</em>0}. Report the test error and sparsity of your model for these different cases.