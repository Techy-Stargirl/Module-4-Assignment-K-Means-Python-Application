# Module-4-Assignment-K-Means-Python-Application
An assignment on constructing a K-Means Python application using a dataset acquired from the Registry of Open Data on AWS. Using PyCharm as an Integrated Development Environment (IDE)

**Assignment Overview**

This assignment involved developing a Python application to implement the K-Means clustering algorithm on a real-world dataset. The primary goal was to segment the data into meaningful, distinct groups (clusters) to uncover underlying patterns and intrinsic structure, providing a foundation for data-driven decision-making. The development was completed in the PyCharm Integrated Development Environment (IDE), adhering to best practices for code efficiency and documentation.

**Dataset Selection and Rationale**
The selected dataset for this project was the Iris Flower Dataset, a collection of 150 instances detailing four features of three species of Iris flower. While this dataset is widely used, it represents the type of tabular, multi-dimensional data frequently found on repositories like the Registry of Open Data on AWS.
The choice was strategic because:
- It is clean and well-structured, simplifying the pre-processing phase.
- It possesses four distinct numerical features, making it an ideal candidate for distance-based clustering.
- The three naturally existing species provide a benchmark against which the K-Means clusters can be visually and analytically validated.

**Technical Approach and Implementation**
- Data Pre-processing: The numerical features were standardised (scaled) using the $Z$-score transformation. This critical step ensures that all features contribute equally to the distance calculation by mitigating the bias towards features with larger magnitudes.
- Optimal Cluster Determination (The Elbow Method): The Within-Cluster Sum of Squares (WCSS) was calculated for $k$ values from 1 to 10. The resulting "Elbow Plot" clearly indicated the optimal number of clusters, $k=3$, which aligns perfectly with the known structure of the Iris data.
- K-Means Execution: The K-Means algorithm was executed with $k=3$. The output included three cluster centroids and a new column assigning each data point to one of the three final clusters.
- Unit Testing: Unit tests were successfully implemented using Python's unittest module to verify the core components, specifically the data scaling correctness (mean $\approx 0$, std $\approx 1$) and the K-Means fitting process (correct number of clusters created).

**Key Findings and Conclusions**
The K-Means application successfully partitioned the dataset into three distinct clusters, providing strong evidence that the four-dimensional feature space naturally organises into three groups.
- Segmentation Success: The resulting clusters closely correspond to the three species of Iris, demonstrating the algorithm's power in unsupervised feature extraction.
- Insight: The cluster centroids, or mean feature values for each cluster, represent three distinct prototypical flower types. For example, Cluster 3 was characterised by the highest values in petal length and width, indicating a larger flower structure.
- Business Impact: For an unknown dataset, this application could be used to segment customers for targeted marketing, categorise sensor data for anomaly detection, or group product features for optimisation, all without prior label knowledge. The robust nature of the code and unit testing ensures reliability for future deployment.
