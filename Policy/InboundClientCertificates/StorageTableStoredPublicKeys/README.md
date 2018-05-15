# Azure Table Storage Public Key Storage for Inbound Client Certificate Policies
- This example uses an Azure Storage Table to store all valid public key thumbprints as rows using a common partition key. 
- You are required to provide (either in-line in set-variable or via a property):
 - The name of the storage account
 - The name of the table to be queried
 - The partition key to be queried
 - A SAS token signed for read/query access to the table listed above
- This expects each thumbprint to be within the RowKey column
- Caching is used to make sure that we don't have the overhead of hitting Azure Storage for every call