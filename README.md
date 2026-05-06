# Project-Milestone

# Film, Color and Brightness
Since my thesis is related to film and color, I am interested in exploring datasets related to movies, such as metadata or image/color analysis.

- Data: Movie datasets (IMDb, Wikipedia)
- Type: Mixed (text + numerical + image data)


### 1) What format should the data use before modeling?

- first I started in a pandas DataFrame for cleaning and inspection.
- Convert to NumPy arrays (or tensors) right before model training.
- Use tensors mainly when training neural networks.

### 2) Does it need encoding, scaling, or normalization?

- Yes, `Genre` is multi-label text and needs encoding.
- Yes, `Year` and engineered numeric features should be scaled.
- Normalization is useful for distance workflows and clustering.

### 3) Should we visualize distributions of features?

- Yes. Plotting feature distributions is required to detect skew, sparsity, imbalance, outliers, and missing-value impact.
- Useful plots for this dataset: year histogram, top-genre frequency bars, and genre co-occurrence summaries.

### 4) Should we use PCA or t-SNE?

- Yes, for exploratory visualization of feature geometry.
- PCA provides a stable linear projection and explained variance.
- t-SNE provides nonlinear neighborhood structure for pattern exploration.
- Neither replaces model evaluation metrics.

### 5) Media-specific analysis for movie posters

- Extract color descriptors (dominant RGB/HEX, brightness) from poster images.
- Plot brightness histograms, top-color frequencies, and brightness-vs-year trends.
- Use these image-derived features together with metadata for clustering/classification.

## Project Notebooks

- `movie_modeling_prep.ipynb`: data preparation, encoding, scaling/normalization, distributions, PCA, t-SNE.
- `movie_poster_color_extraction.ipynb`: poster retrieval + dominant color and brightness extraction + visual analysis.