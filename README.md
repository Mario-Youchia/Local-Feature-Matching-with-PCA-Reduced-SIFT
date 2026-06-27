# Local Feature Matching with PCA-Reduced SIFT

A computer-vision project for matching local features across different views of real-world landmarks. The notebook detects SIFT keypoints, reduces the 128-dimensional descriptors to 32 dimensions with PCA, and applies the nearest-neighbor distance-ratio test.

![Notre Dame feature matches](results/notre-dame-matches.png)

## Project Overview

The notebook implements the complete workflow for:

- Detecting SIFT keypoints and extracting local descriptors.
- Fitting PCA jointly across both descriptor sets.
- Reducing descriptors from 128 dimensions to 32 dimensions.
- Computing nearest-neighbor descriptor distances.
- Applying the nearest-neighbor distance-ratio test.

## Results

| Image pair | Accepted matches | Top 50 accuracy | Top 100 accuracy | All matches |
|---|---:|---:|---:|---:|
| Notre Dame | 595 | 98% | 99% | 91% |
| Mount Rushmore | 406 | 100% | 100% | 99% |
| Episcopal Gaudi | 69 | 86% | — | 86% |

The 32-dimensional PCA descriptors retained approximately 78–80% of the original descriptor variance.

### Mount Rushmore

![Mount Rushmore feature matches](results/mount-rushmore-matches.png)

### Episcopal Gaudi

![Episcopal Gaudi feature matches](results/episcopal-gaudi-matches.png)

The notebook is the canonical implementation. There are no separate source modules or standalone experiment scripts.

## Run the Notebook

The recommended way to run the project is through the Kaggle notebook:

[https://www.kaggle.com/code/marioyouchia/local-feature-matching-with-pca-reduced-sift](https://www.kaggle.com/code/marioyouchia/local-feature-matching-with-pca-reduced-sift)


## Dependencies

- Python
- OpenCV
- NumPy
- pandas
- Pillow
- SciPy
- scikit-image
- scikit-learn
- Jupyter Notebook
