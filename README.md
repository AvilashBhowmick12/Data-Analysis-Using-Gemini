# Data-Analysis-Using-Gemini
###### This is a simplified Google Cloud project using Python Notebook, Cloud Datasets and Gemini

---

# Gemini for Data Scientists: K-means Clustering and Marketing Strategy
## Overview
This project demonstrates the use of Google Colab and BigQuery to perform K-means clustering on ecommerce data and develop a marketing strategy based on the clustering results. The project utilizes various Python libraries and the Vertex AI platform to create a dataset, build a clustering model, and generate insights for a marketing campaign.

Objectives
Use Colab Enterprise Python notebooks inside BigQuery Studio.

Utilize BigQuery DataFrames within BigQuery Studio.

Leverage Gemini to generate code from natural language prompts.

Construct a K-means clustering model to categorize customers.

Visualize the clusters to understand customer segments.

Employ the text-bison model to plan the next steps for a marketing campaign.

Clean up project resources to manage costs and maintain organization.

Setup and Execution
Task 1: Create a BigQuery Dataset
In the Google Cloud console, navigate to BigQuery.
Create a new dataset named ecommerce with a multi-region location in the US.
Task 2: Create a Python Notebook
Create a new Python notebook in BigQuery.
Select the us-central1 region to store code assets.
Task 3: Import Libraries and Define Variables
python
Copy Code
from google.cloud import bigquery
from google.cloud import aiplatform
import bigframes.pandas as bpd
import pandas as pd
from vertexai.language_models._language_models import TextGenerationModel
from bigframes.ml.cluster import KMeans
from bigframes.ml.model_selection import train_test_split
Task 4: Prepare the Ecommerce Dataset
Execute a BigQuery SQL script to create a customer_stats table with relevant ecommerce data.
Task 5: Train the K-means Clustering Model
Split the dataset into training and test sets.

Train the K-means model with 5 clusters.

Save the model to BigQuery.

Task 6: Analyze Clustering Results
Retrieve centroid information from the model.
Generate a prompt for the text-bison model to create a marketing strategy.
Task 7: Clean Up Resources
Delete any unnecessary resources to avoid incurring costs.
Results
The project successfully executed a K-means clustering algorithm on ecommerce data, resulting in the following customer segments:

Cluster 1: Average spend $48.99, 1.28 orders per person, 751.42 days since last order.

Cluster 2: Average spend $58.46, 3.75 orders per person, 774.58 days since last order.

Cluster 3: Average spend $48.07, 1.34 orders per person, 729.71 days since last order.

Cluster 4: Average spend $47.11, 1.31 orders per person, 922.19 days since last order.

Cluster 5: Average spend $234.47, 1.21 orders per person, 804.67 days since last order.

Next Steps
The text-bison model will be used to develop detailed marketing strategies for each cluster, including creative brand personas, catchy titles, and step-by-step actions.

Acknowledgments
Google Cloud Platform for providing the infrastructure and services used in this project.
The developers of the Python libraries and APIs that facilitated the data analysis and model building.
Contributions
Feel free to contribute to this project by suggesting improvements, adding new features, or enhancing the documentation.
