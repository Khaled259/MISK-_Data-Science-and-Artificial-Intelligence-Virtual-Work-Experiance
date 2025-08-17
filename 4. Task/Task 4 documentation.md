### Task 4: Developing a Predictive Car Pricing Model with Azure Machine Learning

#### 🎯 Task Scenario
In the final task, the objective was to build a sophisticated solution to help both the user and the client's marketing team. My mission was to develop a predictive model that could estimate the price of a car based on its features (e.g., make, engine size, mileage). This tool would empower users to get instant price quotes and help the sales team in pricing decisions, ultimately aiming to increase sales.

This required building a **regression model**, and I used the powerful, low-code **Azure Machine Learning Designer** to accomplish this.
#### 🎯 Paths Learned:
[Introduction to machine learning concepts](https://learn.microsoft.com/en-us/training/modules/fundamentals-machine-learning)

---

#### ⚙️ Solution: The Predictive Pipeline Workflow
The entire workflow was designed and executed within an Azure Machine Learning Workspace, following a standard, best-practice machine learning process.

**1. Data Preparation and Preprocessing**
This phase focused on cleaning and preparing the raw data for training.
-   **`Select Columns in Dataset`**: This component acted as the gatekeeper for the pipeline. It was configured to select all relevant predictive features (`Make`, `Model`, `Year`, etc.) and the target label (`Price`), while removing any irrelevant columns (like IDs or columns with excessive missing values) from the raw dataset.
-   **`Clean Missing Data`**: To ensure data quality, this component scanned all selected columns for any null or missing values and was configured to **remove the entire row** if a missing value was found.
-   **`Split Data`**: To ensure an unbiased evaluation of the model, the cleaned dataset was split into two parts: **70% for the training set** (to teach the model) and **30% for the testing set** (to evaluate its performance on unseen data).

**2. Model Training and Prediction**
This phase involved teaching the model and using it to make predictions.
-   **`Linear Regression`**: This component represents the algorithm chosen for the task, which is well-suited for predicting a continuous numerical value like price.
-   **`Train Model`**: This is the core component where the learning happens. It took two inputs: the untrained `Linear Regression` algorithm and the **70% training dataset**. Critically, it was configured here to use the **`Price` column as the Label**—the value it should learn to predict.
-   **`Score Model`**: The trained model was then passed to this component along with the **30% unseen testing dataset**. Its job was to generate a new column containing the model's price predictions for each car in the test set.

**3. Model Evaluation**
-   **`Evaluate Model`**: Finally, the scored dataset (containing both the actual prices and the predicted prices) was fed into this component. It calculates key performance metrics (like R-squared, Mean Absolute Error, etc.) to objectively measure how accurately the model performed.

#### 📈 Pipeline Design and Execution Proof

**1. Machine Learning Pipeline Design**
The visual graph below, built in Azure ML Designer, illustrates the end-to-end workflow from data ingestion to model evaluation.

![Azure ML Designer Pipeline for Car Price Prediction](path_to_your_pipeline_design.png)
> **Note:** Upload your screenshot of the pipeline design and replace `path_to_your_pipeline_design.png` with the actual file path.

**2. Successful Job Execution**
The following screenshot from the "Jobs" panel in Azure ML Studio confirms that the pipeline was executed successfully, processing the data and training the model as designed.

![Screenshot of the Completed Pipeline Job in Azure ML Studio](path_to_your_job_completed.png)
> **Note:** Upload your screenshot of the completed job and replace `path_to_your_job_completed.png` with the actual file path.
