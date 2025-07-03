# Sound Clustering Project

## Overview
This project analyzes and clusters a large set of unlabelled sound (audio) data using a combination of feature extraction, dimensionality reduction, and clustering algorithms. The workflow is implemented in a Jupyter notebook and a Python script, and is designed to help uncover patterns in high-dimensional audio data.

## Tools & Libraries Used
- **Python 3.x**
- **librosa**: For audio loading and feature extraction (Mel-spectrograms)
- **NumPy** and **Pandas**: For data manipulation and analysis
- **Matplotlib** and **Seaborn**: For data visualization
- **scikit-learn**: For dimensionality reduction (PCA, t-SNE) and clustering (KMeans, DBSCAN), as well as evaluation metrics (Silhouette Score, Davies-Bouldin Index)
- **Google Colab**: (Optional) For running the notebook with Google Drive integration

## Workflow Summary
1. **Feature Extraction**: Audio files are loaded and converted into Mel-spectrogram features using `librosa`. Each audio file is represented as a 128-dimensional feature vector.
2. **Visualization**: Initial visualizations of raw features highlight the challenges of high-dimensional data.
3. **Dimensionality Reduction**: Techniques like PCA and t-SNE are used to reduce the feature space to 2 or 3 dimensions for better visualization and clustering.
4. **Clustering**: Both KMeans and DBSCAN algorithms are applied to the original and reduced feature sets. The optimal number of clusters for KMeans is determined using the Elbow method and Silhouette Score.
5. **Evaluation**: Clustering results are evaluated using Silhouette and Davies-Bouldin scores, and visualized in 2D/3D plots.
6. **Analysis**: The effectiveness of different dimensionality reduction and clustering methods is compared and discussed.

## How to Run
### Requirements
Install the required Python packages:
```bash
pip install numpy pandas matplotlib seaborn scikit-learn librosa
```

### Data Preparation
- Place your `.wav` audio files in a directory (the script expects a path to this directory).
- If using Google Colab, upload your data to Google Drive and update the `dataset_path` variable accordingly.

### Running the Notebook
1. Open `clustering_notebook.ipynb` in Jupyter Notebook or Google Colab.
2. Follow the cells sequentially. If using Colab, ensure you mount your Google Drive as shown in the notebook.

### Running the Script
1. Edit `clustering_notebook.py` to set the correct `dataset_path` to your audio files.
2. Run the script:
```bash
python clustering_notebook.py
```

## Notes
- The script and notebook are designed for exploratory analysis and may require adaptation for different datasets or environments.
- For large datasets, t-SNE can be computationally intensive and may take significant time to run.
- Google Colab is recommended for users without a local Python environment or with limited computational resources.

## Results & Interpretation
The project demonstrates the importance of dimensionality reduction for clustering high-dimensional audio data, and compares the effectiveness of KMeans and DBSCAN on both raw and reduced features. See the notebook/script for detailed results and analysis. 