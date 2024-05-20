# demo-service

Problem with ActiveDirectoryManagedIdentity authentication with sleuth dependency.
Service is getting deployed on AKS and db url connection string contains authentication=ActiveDirectoryManagedIdentity.
During Hikari pool initialization service seems freezing and not connecting to db.

To imitate AKS pod put next environment variables(All the properties are generated):
```properties
AZURE_AUTHORITY_HOST=https://login.microsoftonline.com/
AZURE_CLIENT_ID=c0b27f71-5380-49aa-94d9-aeef2cede9b4
AZURE_TENANT_ID=62c0b5e8-e419-4971-9baf-bfc6e22ca200
AZURE_FEDERATED_TOKEN_FILE=./token.txt
```
