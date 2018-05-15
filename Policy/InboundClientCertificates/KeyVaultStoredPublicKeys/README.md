# Azure KeyVault (Secret) Public Key Storage for Inbound Client Certificate Policies
- This example uses an Azure KeyVault Secret to store all valid public key thumbprints seperated by , ; \n \r 
- You are required to provide (either in-line in set-variable or via a property):
 - The Tenant ID of the Azure AD your KeyVault lives within
 - The Application ID for your Service Principal
 - The Application Key/Secret for your Service Principal
 - The KeyVault name
 - The KeyVault Secret name
- The Service Principal must have secret read access to the KeyVault, and Applicaiton permissions to KeyVault.
- Caching is used to make sure that we don't have the overhead of hitting KeyVault for every call