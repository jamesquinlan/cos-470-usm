# COS 470 Lecture Notes

Scribed lecture notes for COS 470 (University of Southern Maine). Each lecture is a LaTeX fragment that is compiled through [`../control.tex`](../control.tex); compiled PDFs live in [`pdfs/`](pdfs/). New lectures should start from [`template.tex`](template.tex).

| # | Topic |
|---|-------|
| [1](#lecture-1--vectors-and-distance-metrics) | Vectors and Distance Metrics |
| [2](#lecture-2--norms-inner-product-and-projection) | Norms, Inner Product, and Projection |
| [3](#lecture-3--dimensionality-distance-and-knn) | Dimensionality, Distance, and KNN |
| [4](#lecture-4--knn-regression-and-scaling) | KNN, Regression, and Scaling |
| [5](#lecture-5--knn-continued) | KNN Continued |
| [6](#lecture-6--model-evaluation-and-the-perceptron) | Model Evaluation and the Perceptron |
| [7](#lecture-7--perceptrons-continued-and-intro-to-svm) | Perceptrons Continued and Intro to SVM |
| [8](#lecture-8--the-perceptron-and-hyperplanes) | The Perceptron and Hyperplanes |
| [9](#lecture-9--regression-loss-functions-and-review) | Regression, Loss Functions, and Review |
| [10](#lecture-10--svm-margins-and-optimization) | SVM Margins and Optimization |
| [11](#lecture-11--svm-primal-and-dual-problems) | SVM Primal and Dual Problems |
| [12](#lecture-12--optimizers-and-intro-to-backpropagation) | Optimizers and Intro to Backpropagation |
| [13](#lecture-13--wrapping-up-svm) | Wrapping Up SVM |
| [14](#lecture-14--gradient-descent-and-momentum) | Gradient Descent and Momentum |
| [15](#lecture-15--gradient-descent-variants-and-adaptive-optimizers) | Gradient Descent Variants and Adaptive Optimizers |
| [16](#lecture-16--calculus-review-and-backpropagation) | Calculus Review and Backpropagation |
| 17 | *(no notes)* |
| [18](#lecture-18--backpropagation-introduction) | Backpropagation Introduction |
| [19](#lecture-19--neural-network-architecture-and-training) | Neural Network Architecture and Training |

---

### Lecture 1 — Vectors and Distance Metrics
**Source:** [`1.tex`](1.tex)

Introduces vectors as points in $\mathbb{R}^p$ and the abstract notion of a distance metric (a non-negative function of two vectors). Works through common metrics — Euclidean, Manhattan, Chebyshev, and Hamming (via the binary indicator function) — with examples, and closes with exploration (XPL) problems.

### Lecture 2 — Norms, Inner Product, and Projection
**Source:** [`2.tex`](2.tex)

Defines a norm and its axioms, relating it to length and distance ($\|x\| = d(x, 0)$). Visualizes the $L_2$ and Chebyshev unit balls, then covers the inner product and vector projection.

### Lecture 3 — Dimensionality, Distance, and KNN
**Source:** [`3.tex`](3.tex)

Reviews vector spaces and distance, then digs into the curse of dimensionality (the box-size problem, volume analysis) and motivates dimensionality reduction. Implements distance metrics in Julia, formalizes metric properties, and introduces the K-Nearest Neighbors algorithm: steps, why it works, a classification example, choosing $k$, computational complexity, and handling missing data.

### Lecture 4 — KNN, Regression, and Scaling
**Source:** [`4.tex`](4.tex)

Applies KNN to regression, including feature representation, a use case, and cross-validation. Covers data preprocessing and scaling techniques, an outline of the KNN algorithm, and the classifier function (`argmax`/`argmin`, the mode). Ends with class code and explorations.

### Lecture 5 — KNN Continued
**Source:** [`5.tex`](5.tex)

Finishes the previous lecture's min–max scaling (mapping $[a, b] \to [0, 1]$), discusses more properties of kNN, and walks through a Julia implementation, followed by XPLs.

### Lecture 6 — Model Evaluation and the Perceptron
**Source:** [`6.tex`](6.tex)

Reviews KNN and how to evaluate a model: cross-validation, grid search, accuracy, error rate, precision, recall, specificity, and F-score. Introduces the Perceptron algorithm (with a nod to the kernel trick) and closes with exploration problems.

### Lecture 7 — Perceptrons Continued and Intro to SVM
**Source:** [`7.tex`](7.tex)

Places the perceptron within supervised learning (vs. unsupervised) and its categories, discusses linear separability, the set of all decision functions, and the perceptron's limitations. Introduces Support Vector Machines and their prerequisites; includes XPLs.

### Lecture 8 — The Perceptron and Hyperplanes
**Source:** [`8.tex`](8.tex)

A deeper look at the perceptron: the geometry and mathematical definition of a hyperplane in different dimensions, the "bundle & save" bias trick, linear separability assumptions, the training goal, why $\mathbf{w}$ is perpendicular to the hyperplane, the classifier equation, and the class code for the perceptron algorithm.

### Lecture 9 — Regression, Loss Functions, and Review
**Source:** [`9.tex`](9.tex)

Contrasts regression with classification and introduces loss functions — zero-one, absolute, and squared — along with cost vs. loss, the objective function (cost + regularizer), and gradient descent. Reviews the perceptron and KNN from earlier lectures and provides practice problems.

### Lecture 10 — SVM Margins and Optimization
**Source:** [`10.tex`](10.tex)

Covers SVM margins and the objective $\min \tfrac{1}{2}\|\mathbf{w}\|^2$ subject to $y_i(\mathbf{w}^T\mathbf{x}_i + b) \ge 1$, the weight vector as a weighted sum of support vectors, Lagrange multipliers for constrained optimization, partial derivatives and gradients, and gradient descent.

### Lecture 11 — SVM Primal and Dual Problems
**Source:** [`11.tex`](11.tex)

Uses monotonic functions to justify the maximum-margin reformulation, sets up the SVM primal problem, derives the dual via Lagrange multipliers, and practices computing the gradient of the loss function.

### Lecture 12 — Optimizers and Intro to Backpropagation
**Source:** [`12.tex`](12.tex)

Presents the RMSProp and Adam optimizers, then reviews differential calculus (derivatives, the chain rule) in the context of minimizing cost. Applies the chain rule to a small neural network to introduce the backpropagation flow.

### Lecture 13 — Wrapping Up SVM
**Source:** [`13.tex`](13.tex)

Finishes SVM by optimizing the dual $f(\alpha)$ to recover $\mathbf{w}$ and $b$. Shows why the direct method is problematic, turns to indirect (iterative, gradient-based) methods and their update rule, discusses kernelization, and motivates backpropagation and deep learning for non-linear data.

### Lecture 14 — Gradient Descent and Momentum
**Source:** [`14.tex`](14.tex)

Frames optimization as finding $\arg\min$/$\arg\max$, contrasting exact and iterative methods. Covers vanilla gradient descent, momentum, Nesterov Accelerated Gradient (NAG), and a gradient-based Nesterov formulation.

### Lecture 15 — Gradient Descent Variants and Adaptive Optimizers
**Source:** [`15.tex`](15.tex)

Discusses issues with batch gradient descent and the related stochastic and mini-batch variants, then surveys momentum, NAG, AdaGrad, RMSProp, and Adam, including the features and drawbacks of each.

### Lecture 16 — Calculus Review and Backpropagation
**Source:** [`16.tex`](16.tex)

A math review for backpropagation: function types and domains, the derivative from first principles, the power rule via binomial expansion, product/quotient/chain rules, and multivariable derivatives (gradients, vector-valued functions), with exercises. Then introduces backpropagation.

### Lecture 18 — Backpropagation Introduction
**Source:** [`18.tex`](18.tex)

Reviews derivative rules, the chain rule, and Leibniz notation, introduces activation functions, works through backpropagation on a neural network example, and includes two code examples.

### Lecture 19 — Neural Network Architecture and Training
**Source:** [`19.tex`](19.tex)

Describes how to train a network (forward feed → cost → backpropagation → update), feedforward network structure, indexing notation, and the matrix representation. Covers cost function minimization, the backpropagation algorithm, applying the chain rule, and the weight update.

---

### Supplemental

- [`lecture_0414.tex`](lecture_0414.tex) — Notes from 04/14 on RMSProp and Adam, the calculus review for backpropagation, and a forward/backward pass through a neural network (overlaps with Lecture 12).
- [`template.tex`](template.tex) — Starter template for new lecture notes.
