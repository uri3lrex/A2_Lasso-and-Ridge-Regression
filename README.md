Data: 2 input features, real-valued target.

What I did

3D scatter of the data; the points lie on a curved surface, not a plane.
Expanded to all polynomial features up to degree 5 (20 features).
Trained Lasso (L1) and Ridge (L2) over a wide range of C, reporting each parameter by feature name.
Plotted prediction surfaces on a grid extending beyond the data to compare under-fit, well-fit and over-fit models.
Used 5-fold cross-validation with error bars (mean ± std of the error vs C) to choose C, against a mean-predictor baseline.

Results

Lasso sets parameters to exactly zero at small C and switches features on as C grows, giving a sparse model.
Ridge shrinks every parameter smoothly but keeps them all non-zero.
Small C under-fits (flat surface); large C over-fits (surface bends to individual points, and extrapolation outside the data goes wrong).