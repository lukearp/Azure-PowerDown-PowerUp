# What does this do?
Deploys to an Azure Function app.  Has two powershell functions with Time Triggers to Power Up and Power Down azure resources base on a Tag Key and Value.  

PowerUp tag = AutoStart: True
PowerDown tag = AutoStop: True

If the tag and value isn't present on the resource it is ignored.  

Currently supports the following Azure Resources:

Virtual Machines
VM Scale Sets
MySQL DB Flexible Servers
Azure Firewall (PowerDown only)

# What does the function require?
System Managed Idenitity enabled and scoped to an Azure Subscription.  Function currently only supports managing power state of resources in a single Azure Subscription.  

# Deployment

[![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Flukearp%2FAzure-PowerDown-PowerUp%2Fmaster%2Ffunction-app.json)