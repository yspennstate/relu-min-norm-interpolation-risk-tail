# The risk tail of minimum-norm ReLU interpolation on the sphere

Yitzchak Shmalo

Paper: [paper/main.pdf](paper/main.pdf)

Two-layer ReLU networks without biases are fitted to n independent Rademacher labels at independent uniform points of the unit sphere in R^d, choosing the interpolant with the smallest Euclidean norm of the weights. Joshi, Vardi and Srebro showed that for univariate networks with biases the expected squared risk of minimum-norm interpolants of noisy labels is infinite. In the bias-free model on the sphere, at every fixed sample size n >= 3, the tail of the squared risk R satisfies

    P(R > t) ≍ t^{-(d-1)/2}   as t -> infinity,

from above and from below. So E[R] is infinite for d = 2, 3 and finite for d >= 4, and more generally E[R^r] is finite exactly when r < (d-1)/2.

The lower bound comes from a close pair of inputs with opposite labels and the other inputs on one side of the plane between them. The upper bound comes from an explicit interpolant built from tents, whose cost is controlled by the smallest angle between two input lines.

## Contents

- `paper/main.tex`, `paper/notation.tex`: LaTeX source.
- `paper/main.pdf`: the compiled paper.
- `code/check_tents.py`: numerical checks of the explicit interpolant used in the upper bound (requires numpy; prints ALL PASS).
