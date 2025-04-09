# Transform-data-using-Spark
# Transform Data Using Spark in Synapse Analytics

In this guide, you will learn how to transform data using **Apache Spark** within **Azure Synapse Analytics**. Data engineers often use Spark notebooks for **ETL (Extract, Transform, Load)** or **ELT (Extract, Load, Transform)** tasks, enabling them to transform data from one format or structure to another.

## Prerequisites

Before you start this exercise, you will need:

- An **Azure Subscription** with administrative-level access.
- **Azure Synapse Analytics Workspace** provisioned with access to **Data Lake Storage** and an **Apache Spark pool**.

## Estimated Completion Time
Approximately **30 minutes**.

## Setup Azure Synapse Analytics Workspace

To provision an **Azure Synapse Analytics** workspace, follow these steps:

### 1. Sign in to the Azure portal
Go to [Azure Portal](https://portal.azure.com).

### 2. Open the Cloud Shell
- Use the `[>_]` button next to the search bar at the top of the page to create a new Cloud Shell in the Azure portal.
- Choose the **PowerShell** environment and create storage if prompted.

### 3. Clone the GitHub Repository
In the Cloud Shell, enter the following command to clone the repository:

```bash
rm -r dp-203 -f
git clone https://github.com/MicrosoftLearning/dp-203-azure-data-engineer dp-203
```

### 4. Run the Setup Script
Once the repository has been cloned, change to the relevant folder and run the setup script:
```bash
cd dp-203/Allfiles/labs/06
./setup.ps1
```
###5. Configure the Script
-If prompted, select the subscription you want to use (this will only appear if you have multiple subscriptions).
-Enter a password for the Azure Synapse SQL pool when prompted. Make sure to remember this password.
-Wait for the script to complete, which typically takes around 10 minutes, but may take longer depending on your environment.

#Use Spark Notebook to Transform Data
After the script completes, you can proceed with transforming the data.

##1. Access Your Synapse Workspace
-Go to the resource group (dp203-xxxxxxx) created by the script in the Azure portal.
-Open your Synapse Workspace.

##2. Open Synapse Studio
-In the Synapse Workspace Overview, click on Open Synapse Studio to open Synapse Studio in a new browser tab.

##3. Verify Spark Pool
-In Synapse Studio, go to the Manage page.
-Select the Apache Spark pools tab and ensure that a Spark pool (e.g., sparkxxxxxxx) is provisioned.

##4. Verify Data Lake Storage Link
-On the Data page, select the Linked tab.
-Check that your Azure Data Lake Storage Gen2 is linked to your workspace.

##5. Explore the Data Files
-Expand your storage account and go to the files container.
-Inside the files container, you’ll see two folders: data and synapse. The data folder contains the sales data files.

##6. Preview the Data
-Open the data folder and preview one of the .csv files.
-Ensure that the file contains a header row.

##7. Download the Notebook
-Download the Spark Transform.ipynb file from the repository folder Allfiles/labs/06/notebooks.
-You can either copy the text and save it manually or download the file directly from the GitHub repository.

#Import the Notebook in Synapse Studio

##1. Import the Notebook
-In Synapse Studio, navigate to the Develop page.
-Expand Notebooks, click on + Import, and select the Spark Transform.ipynb file you just downloaded.

##2. Attach the Notebook to Spark Pool
-Attach the notebook to your Spark pool (sparkxxxxxxx).

##3. Run the Notebook
-Review the notes in the notebook and run the code cells to perform the data transformation.

