# University Segmentation with K-Means Clustering

Groups **777 US universities** into two clusters with **K-Means** (unsupervised), then checks how well the clusters match the real *Private / Public* label.

> 📚 **Course project:** completed while following the Udemy course *Python for Data Science and Machine Learning Bootcamp* (Pierian Data). The dataset and task come from the course.

## Data (`College_Data`)
777 universities with 17 numeric features, e.g. applications, acceptances, enrolment, out-of-state tuition, % faculty with PhD, student/faculty ratio, expenditure per student and graduation rate. The `Private` label is **not** used for clustering, only for evaluation.

## Approach
1. Exploratory analysis (Seaborn): tuition vs. graduation rate, distributions by type
2. Fixed a data error: a graduation rate above 100%
3. **K-Means** with *k = 2* (scikit-learn)
4. Compared the clusters with the true labels (confusion matrix and classification report)

## Results
The clusters match the Private/Public label for **78%** of universities (weighted F1 0.75). Because K-Means never sees the labels, this shows how well the features separate the two groups on their own.

## Tech
Python · pandas · NumPy · scikit-learn · Matplotlib · Seaborn · Jupyter

## Run it
```bash
git clone https://github.com/Aniket1103200/kmeans-university-segmentation.git
cd kmeans-university-segmentation
pip install -r requirements.txt
jupyter notebook kmeans_university_clustering.ipynb
```
