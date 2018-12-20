# Azure Serverless Contact Form

> Simple serverless application that sends an email using Azure Functions and SendGrid.

This demo application contains a static HTML contact page and a JavaScript-based function that uses the Azure Functions Runtime 2.0. The HTML page can be served from Azure Storage. When users fill out and submit the form, it invokes the function and sends the form details via email using SendGrid.

## Deployment Steps

Eventually, I will include deployment automation for this project. For now, you can follow these high-level steps to manually deploy this application to Azure.

* Create an Azure Storage account. Enable [static website hosting](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website) and upload the **index.html** file from the **www** folder of this repo into the **$www** container in the storage account.
* [Create a SendGrid Account](https://docs.microsoft.com/en-us/azure/sendgrid-dotnet-how-to-send-email#create-a-sendgrid-account) in the Azure Portal and create a SendGrid API key in the SendGrid console.
* Create an App Setting entry in your Function App called **SendGrid** that contains your SendGrid API key.
* Deploy the **ContactFormAPI** in this repo to your Function App. You can do this easily with Visual Studio (VS) Code using the steps outlined in [Deploy to Azure using Azure Functions](https://code.visualstudio.com/tutorials/functions-extension/getting-started).

## App Preview
![alt text](https://user-images.githubusercontent.com/5126491/50303670-038ad800-044b-11e9-9488-04f94e2843a6.gif "README Image")

## App Info

### Author

Mike Pfeiffer
[@mike_pfeiffer](https://twitter.com/mike_pfeiffer)

### Version

1.0.0

### License

This project is licensed under the Apache License 2.0

