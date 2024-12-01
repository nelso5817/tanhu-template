``` mermaid
graph TD
    A(Canvas Power App) --> | Submit data | B[(SharePoint List)] --> C(Power Automate Approval Flow) --> D(Logic App) --> E(Entra ID App) <--> | Secret stored in Key Vault | F(Azure Key Vault) --> G{Type of collaboration space} --> |SharePoint Site| H[SharePoint REST API] 
    G --> | Office 365 Group | I(Microsoft Graph)
    G --> | Viva Engage Community | J(Microsoft Graph) 
    I --> K(Azure Automation)
    H --> K
    J --> K
    K --> | Additional configuration using Managed Identity | L(PnP PowerShell) --> M(Provisioned space)
``````


``` mermaid
sequenceDiagram
    participant Alice
    participant Bob
    Alice->>Bob: Hello Bob, how are you?
    Bob-->>Alice: I am good, thanks!
``````
