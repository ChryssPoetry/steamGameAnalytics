Steam Games Analytics
This project focuses on analyzing and deriving actionable insights from the Steam Games dataset. The workflow includes data cleaning, sending data to Firebase, integrating with Google BigQuery, and creating visualizations in Tableau for better decision-making.

Table of Contents
Project Overview
Workflow
1. Data Cleaning
2. Firebase Integration
3. Google BigQuery Integration
4. Visualizations with Tableau
Technologies Used
Setup Instructions
Future Enhancements
Project Overview
Steam Games Analytics provides insights into the gaming industry by leveraging Machine Learning (ML) techniques, Firebase, and Tableau dashboards. Key highlights include:

Building a recommendation system to suggest games based on player preferences.
Predicting game success metrics using ML models.
Forecasting trends in game genres using time-series analysis.
Visualizing key insights for better decision-making.
Workflow
1. Data Cleaning
We started with raw data and performed the following steps:

Handled missing values (NaN) by replacing them with defaults or dropping rows where necessary.
Engineered new features, such as:
Total Reviews: Combined Positive and Negative reviews.
Estimated Revenue: Calculated as Price * Positive reviews.
Success Metric: Defined based on Peak CCU (Peak Concurrent Users).
Removed outliers to improve model accuracy (e.g., games with extreme revenue or price values).
2. Firebase Integration
After cleaning, the processed data was sent to Firebase for centralized storage:

Setup Firebase: Created a Firebase project and enabled Realtime Database.
Data Upload:
Used the Firebase Admin SDK to programmatically upload data.
Converted the dataset to JSON format for compatibility with Firebase.
3. Google BigQuery Integration
Firebase data was exported to Google BigQuery for advanced querying and reporting:

Enabled BigQuery export in Firebase Console.
Verified that the synced data appeared as a dataset in BigQuery.
Built SQL queries in BigQuery to prepare data for Tableau visualizations.
4. Visualizations with Tableau
The cleaned and processed data was visualized using Tableau:

Connected Tableau to BigQuery for real-time data updates.
Built dashboards to:
Display top games by player count and revenue estimates.
Visualize genre trends over time.
Provide recommendations based on game attributes.
Technologies Used
Technology	Purpose
Python	Data cleaning, preprocessing, ML modeling
Pandas	Data manipulation and cleaning
Firebase Admin SDK	Uploading data to Firebase
Google BigQuery	Advanced querying and integration
Tableau	Data visualization and dashboard creation
Streamlit	Interactive web-based recommendation tool
Scikit-learn	Machine learning models
TensorFlow	Advanced deep learning models
Setup Instructions
Prerequisites
Python (>= 3.8)
Firebase Project (with Realtime Database enabled)
Google BigQuery (linked to Firebase)
Tableau Desktop

python upload_to_firebase.py
Connect Firebase to Google BigQuery:

Enable BigQuery integration in Firebase Console.
Verify that the dataset appears in BigQuery.
Visualize data in Tableau:

Connect Tableau to BigQuery.
Use provided templates to create dashboards.
Run the Streamlit app (optional):

bash
streamlit run dashboard.py
Future Enhancements
Real-Time Updates:

Automate data sync between Firebase and BigQuery.
Enable live dashboards in Tableau.
Advanced Machine Learning:

Build collaborative filtering recommendation systems.
Deploy deep learning models for sentiment analysis.
Enhanced Visualizations:

Add more interactivity to Tableau dashboards.
Use geospatial visualizations for region-specific insights.
Deploy as a Web App:

Integrate recommendations and insights into a fully hosted web application.
Contributing
Contributions are welcome! Please submit a pull request or raise an issue for suggestions.

License
This project is licensed under the MIT License.

