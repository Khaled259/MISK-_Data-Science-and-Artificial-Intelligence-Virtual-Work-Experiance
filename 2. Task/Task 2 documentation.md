### Task 2: Building a Data Ingestion Pipeline with Azure Data Factory

#### 🎯 Task Scenario
Following the environment setup in Task 1, the next objective was to begin the data migration process. As part of the development team, my role was to simulate the ingestion of data from a disparate source (represented by an `emp.txt` file) and move it into our centralized Azure Storage Account. This is a foundational step in any data analytics or AI project.

---

#### ⚙️ Workflow Implemented
The task was accomplished by building a data copy pipeline using the Azure Data Factory (ADF) Studio.

1.  **Data Staging:**
    -   First, the source data file (`emp.txt`) was manually uploaded to a blob container named `adftutorial` inside a folder designated as `input`. This simulates the availability of raw data ready for processing.
    -   ![Screenshot of the adftutorial container](https://github.com/Khaled259/MISK-_Data-Science-and-Artificial-Intelligence-Virtual-Work-Experiance/blob/17d922330e61abed0fe8b032a23740b2d65276ff/2.%20Task/1.%20adftoturial%20Blob%20Container.png)

2.  **Pipeline Creation using Azure Data Factory:**
    -   Using the **Copy Data tool** in ADF, a new pipeline was configured.
    -   **Source Configuration:** A new connection was established to our Azure Blob Storage account, and the `input/emp.txt` file was set as the source dataset.
    -   **Destination (Sink) Configuration:** The same storage account was used as the destination, with the target folder path set to `adftutorial/output`.
    -   **Binary Copy:** The "Binary copy" option was selected to ensure the file was transferred exactly as-is, without any schema modifications.

3.  **Pipeline Execution and Monitoring:**
    -   The pipeline was triggered, and the run was monitored through the ADF "Monitor" tab to confirm its successful execution.
      

#### 📄 Deliverable
A screenshot of the "Deployment complete" page in Azure Data Factory, confirming that the pipeline ran successfully and the `emp.txt` file was copied from the `input` folder to the `output` folder.

![Screenshot of successful ADF Pipeline run](https://github.com/Khaled259/MISK-_Data-Science-and-Artificial-Intelligence-Virtual-Work-Experiance/blob/53a7b889eb2b54f4bfb33fa0a58033e1d547d204/2.%20Task%20/2.Deployment%20Complete.png)

 ![Screenshot of the adftutorial container outputfolder](https://github.com/Khaled259/MISK-_Data-Science-and-Artificial-Intelligence-Virtual-Work-Experiance/blob/17d922330e61abed0fe8b032a23740b2d65276ff/2.%20Task/4.%20output%20folder.png)
