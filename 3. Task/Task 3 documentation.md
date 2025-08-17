### Task 3: Building an Image Classification Model with Custom Vision

#### 🎯 Task Scenario
Building on the successful data pipeline from Task 2, my manager assigned the next phase: enhancing the user experience on the client's platform with AI. The long-term vision is a feature where users can upload a car photo, and the system automatically identifies its make, model, and specifications.

As a foundational first step, my task was to develop a proof-of-concept model that could solve a simpler problem: **classifying whether an uploaded image contains a car or not.**

#### 🎯 Paths learned
    1. [Introduction to computer vision concepts](https://learn.microsoft.com/en-us/training/modules/introduction-computer-vision)
    [Visually monitor Azure Data Factory](https://learn.microsoft.com/en-us/azure/data-factory/monitor-visually)

---

#### ⚙️ Solution and Workflow
To tackle this, I used **Azure's Custom Vision service**, an AI tool designed for building specialized image classifiers with ease.

1.  **Resource Provisioning:**
    -   In the Azure portal, I created the necessary **Custom Vision resources** (both Training and Prediction instances) to host the project.

2.  **Project Setup in Custom Vision Studio:**
    -   A new project was created with the following configuration:
        -   **Project Type:** `Classification`
        -   **Classification Type:** `Multiclass` (each image gets a single tag)
        -   **Domain:** `General` (optimized for a wide variety of images)

3.  **Data Preparation and Training:**
    -   I curated and uploaded a dataset of images, carefully tagging each one as either `car` or `not_car`.
    -   The dataset included a variety of images (different camera angles, lighting, backgrounds) to ensure the model could generalize well, following best practices for training.

4.  **Model Training and Evaluation:**
    -   I initiated the training process. Custom Vision uses the tagged images to build a model that learns the visual characteristics of each class.
    -   After training, the model's performance was evaluated. The key metric for this task was **Precision**, which measures the accuracy of the positive predictions.

#### 📄 Results and Deliverable
The model successfully met the project's requirement. The deliverable was a screenshot of the model's performance results, demonstrating a **Precision score of 60% or higher.**

![Screenshot of Custom Vision Model Performance](https://github.com/Khaled259/MISK-_Data-Science-and-Artificial-Intelligence-Virtual-Work-Experiance/blob/9746296a019c833470c0f92ae389f9cb9e8c08b5/3.%20Task/2.%20Model%20Performance.png)
