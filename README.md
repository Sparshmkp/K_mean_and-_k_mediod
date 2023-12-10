**Code Explanation of K-Means:**
Step 1: Begin by importing essential libraries such as pandas, numpy, and matplotlib.
Step 2: Load the dataset provided in the assignment.
Step 3: Remove the columns "id," "diagnosis," and "Unnamed:32." The "id" column serves as a
unique identifier, and the "diagnosis" column indicates cancer types ("M" for malignant or "B" for
benign). While these columns are valuable for understanding and categorizing the data, they are
not suitable for clustering, which focuses on similarities between data points based on their
features.
Step 4: Specify the desired number of clusters.
Step 5: Set a random seed using `np.random.seed(0)` to ensure reproducibility. Initialize cluster
centroids by randomly selecting data points.
Step 6: Initialize a label array with zeros to store cluster assignments for each data point. `labels
= np.zeros(pdf.shape[0])`
Step 7: The main loop of the K-Means algorithm begins. In each iteration:
● Assign each data point to the nearest centroid based on Euclidean distance.
● Compute new centroids by calculating the mean of data points in each cluster.
● Check for convergence by comparing the old centroids with the new centroids. If they
are very close, break the loop.
Step 8: Visualize the data points using different colors based on their assigned clusters.
Step 9: Calculate the number of data points in each cluster.
**Code Explanation of K-Medoid:**
Step 1: Begin by importing essential libraries like pandas, numpy, and matplotlib.
Step 2: Load the dataset provided in the assignment.
Step 3: Drop the columns "id," "diagnosis," and "Unnamed:32" because they don't contribute to
clustering. "id" is a unique identifier, and "diagnosis" represents cancer types, which aren't
suitable for clustering. Clustering relies on the similarities between data points based on their
features.
Step 4: Determine the desired number of clusters.
Step 5: Set a random seed using np.random.seed(0) to ensure reproducibility. Initialize cluster
centroids by randomly selecting data points.
Step 6: Utilize the Manhattan distance function to calculate the distance between two points.
Unlike Euclidean distance, which measures straight-line distance, Manhattan distance considers
the "city block" or "taxicab" distance between points.
Step 7: Initialize a label array with zeros to store cluster assignments for each data point.
labels = np.zeros(pdf.shape[0])
Step 8: The main loop of the K-Medoids algorithm begins. In each iteration:
● Assign each data point to the nearest medoid based on Manhattan distance.
● Update medoids by selecting the point within the same cluster that has the smallest
total Manhattan distance to others.
● Check for convergence by comparing old medoids with new medoids. If they are very
close, break the loop.
Step 9: Visualize the data points with different colors based on their assigned clusters.
Step 10: Calculate the number of points in each cluster.
