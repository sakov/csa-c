## csa ##
(Cubic Spline Approximation)

**csa** is a C code for cubic spline approximation of 2D scattered data. It provides a C library and a command line utility **csabathy**.

**csa** uses a fast O(N) and robust algorithm that works nicely for uniformly distributed data. It is described in [this](http://dx.doi.org/10.1109/VISUAL.2001.964530) paper. For clustered data you may prefer Natural Neighbours interpolation.

Checkout csa by running `git clone https://github.com/sakov/csa-c` or `svn checkout https://github.com/sakov/csa-c`.

From the [original paper](http://dx.doi.org/10.1109/VISUAL.2001.964530):

*We have presented an efficient method to automatically compute smooth approximations of large sets of unorganized scattered data points. The method is based on the construction of a differentiable bivariate spline with respect to a uniform triangle mesh over an arbitrarily shaped planar domain. For a uniformly distributed subset of triangles we compute local polynomial least squares approximations by using singular value decomposition (SVD) of small matrices. The smooth approximating spline is constructed by gluing together these patches using Bernstein-Bézier smoothness conditions. We emphasize the following key features of our method:*

- *We develop a completely local approach, which means that we do not use any global optimization or other techniques involving computation with large portions of the data set.*

- *We employ the rank-revealing features of SVD to control the polynomial degree of the initial patches, which allows to take into account the local variation and distribution of the data points.*

- *The algorithm does not make use of any interpolation scheme. In particular, no estimation of derivatives is needed.*

- *Our method offers optimal approximation order and the constructed spline is by its nature C1-continuous. In addition, the spline surface does not have artifacts like, for instance, peaks or flat spots close to the data points.*

- *The use of a uniform triangle mesh also contributes to great savings in computation time. As a result, the overall complexity of the algorithm is linear in the number of scattered data points.*
