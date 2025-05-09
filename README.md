# COS 470 University of Southern Maine
Topics in Computer Science: Mathematics of Machine Learning


## Topics - Student Scribed Notes
1. [Vectors and distance metrics](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/1.tex)
2. [Scalar product, Norms, Projections](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/2.tex)
3. [Curse of Dimensionality](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/3.tex)
4. [Intro. to k-NN](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/4.tex)
5. [k-NN continued w/code](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/5.tex)
6. [Cross Validation & Perceptron](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/6.tex)
7. [Perceptron cont. Intro to SVM](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/7.tex)
8. [Perceptron cont. Intro to Hyperplanes](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/8.tex)
9. [Regression & Loss](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/9.tex)
10. [Margins & Lagrange Multipliers](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/10.tex)
11. [SVM Optimizing](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/11.tex)
12. [Optimizers & Intro to Intro to Backpropagation](https://github.com/jamesquinlan/cos-470-usm/blob/main/lectures/12.tex)

## Software and Platforms

* [Julia](https://julialang.org)
* [Python](https://www.python.org)
* [Google Colab](https://colab.research.google.com)
* [Jupyter Notebooks](https://jupyter.org)


## Related Links

* [LaTeX in 30 minutes](https://www.overleaf.com/learn/latex/Learn_LaTeX_in_30_minutes)
* [LaTeX Tutorials](https://www.overleaf.com/learn/latex/Tutorials)
* [LaTeX Symbols](https://www.cmor-faculty.rice.edu/~heinken/latex/symbols.pdf)
* [Mathematics Subject Classification](https://mathscinet.ams.org/mathscinet/msc/msc2020.html)
* [PGFPlots Gallery](https://pgfplots.sourceforge.net/gallery.html)
* [Table Generator](https://www.tablesgenerator.com)
* [TikZ 1](https://www.overleaf.com/learn/latex/TikZ_package)
* [TikZ Examples](https://texample.net)


## Setup

To work on your local machine or on a cloud based platform (e.g., Overleaf), you need the following:

1. `control.tex`  (this is the main control file.  Only edit definitions (`\def`) at the top with specific information
2. `packages.tex` (containing all the packages)
3. `code.tex`  (packages for code snippets, `packages.tex` calls this as input) 
4. `reference.bib` (bibTeX database)
5. `lectures` directory.  Your notes should be in this directory and **NOT** contain document class, begin document or end document statements, but **ONLY** the notes you scribed.  The documentclass, etc. are contained in the control file.
