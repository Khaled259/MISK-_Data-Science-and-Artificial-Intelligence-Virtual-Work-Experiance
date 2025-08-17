### Task 4: Developing a Predictive Car Pricing Model with Azure Machine Learning

#### 🎯 Task Scenario
In the final task, the objective was to build a sophisticated solution to help both the user and the client's marketing team. My mission was to develop a predictive model that could estimate the price of a car based on its features (e.g., make, engine size, horsepower). This tool would empower users to get instant price quotes and help the sales team in pricing decisions, ultimately aiming to increase sales.

This required building a **regression model**, and I used the powerful, low-code **Azure Machine Learning Designer** to accomplish this.

---

#### ⚙️ Solution: Building the Predictive Pipeline
The entire workflow was designed, built, and executed within an **Azure Machine Learning Workspace**.

1.  **Data Ingestion and Preparation:**
    -   The project started with the "Automobile price data (Raw)" dataset, which was registered as a formal dataset asset in the workspace.
    -   **Data Preprocessing:** Key cleaning steps were performed to prepare the data for training:
        -   `Select Columns in Dataset`: Excluded columns with a high number of missing values to improve model quality.
        -   `Clean Missing Data`: Removed rows with any remaining missing values.
        -   `Split Data`: The cleaned dataset was divided into two parts: **70% for training** the model and **30% for testing** its performance.

2.  **Model Training and Scoring:**
    -   **Algorithm Selection:** A **Linear Regression** algorithm was chosen as the model for predicting the continuous price value.
    -   **Training:** The `Train Model` component used the 70% training data subset to teach the Linear Regression algorithm the relationship between car features and price.
    -   **Scoring:** The `Score Model` component then used the trained model to make predictions on the unseen 30% test dataset.

3.  **Model Evaluation:**
    -   Finally, the `Evaluate Model` component was used to assess the performance of the model by comparing the predicted prices against the actual prices from the test set. This step generates key metrics (like R-squared, Mean Absolute Error, etc.) to determine the model's accuracy.

#### 📄 Results and Deliverable
The entire machine learning pipeline was successfully built and executed in Azure Machine Learning Designer. The deliverable was a screenshot of the completed pipeline, showing the logical flow from raw data to a trained and evaluated model.

![Screenshot of the complete Azure ML Designer Pipeline for Car Price Prediction](path_to_your_task4_pipeline.png)
> **Note:** Remember to upload your screenshot of the final pipeline and replace `path_to_your_task4_pipeline.png` with the actual file path.
