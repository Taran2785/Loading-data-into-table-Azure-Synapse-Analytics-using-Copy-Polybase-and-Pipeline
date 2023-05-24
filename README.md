# Loading-data-into-table-Azure-Synapse-Analytics-using-Copy-Polybase-and-Pipeline

**COPY INTO (Transact-SQL)**

The COPY statement provides the most flexibility for high-throughput data ingestion into Azure Synapse Analytics.

**Use COPY for the following capabilities**:

Use lower privileged users to load without needing strict CONTROL permissions on the data warehouse.

Execute a single T-SQL statement without having to create any other database objects.

Properly parse and load CSV files where delimiters (string, field, row) are escaped within string delimited columns.

Specify a finer permission model without exposing storage account keys using Share Access Signatures (SAS).

Use a different storage account for the ERRORFILE location (REJECTED_ROW_LOCATION).

Customize default values for each target column and specify source data fields to load into specific target columns.

Specify a custom row terminator for CSV files.

Use SQL Server Date formats for CSV files.

Specify wildcards and multiple files in the storage location path.

Automatic schema discovery simplifies the process of defining and mapping source data into target tables.

The automatic table creation process automatically creates the tables and works alongside with automatic schema discovery.

**Design a PolyBase data loading strategy for dedicated SQL pool in Azure Synapse Analytics**

The fastest and most scalable way to load data is through PolyBase. PolyBase is a technology that accesses external data stored in Azure Blob storage or Azure Data Lake Store via the T-SQL language.

The basic steps for implementing a PolyBase ELT for dedicated SQL pool are:

Extract the source data into text files.

Land the data into Azure Blob storage or Azure Data Lake Store.

Prepare the data for loading.

Load the data into dedicated SQL pool staging tables using PolyBase.

Transform the data.

Insert the data into production tables.

**Build a data pipeline in Azure Synapse Analytics**

Provision an Azure Synapse Analytics workspace

View source and destination data stores

Implement a pipeline

Create a pipeline with a Copy data activity

Data mapping

Review and Finish
