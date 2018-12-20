# Azure Serverless Contact Form

> Simple serverless application that sends an email using Azure Functions and SendGrid.

This demo application contains a static HTML contact page and a JavaScript-based function that uses the Azure Functions Runtime 2.0. The HTML page can be served from Azure Storage. When users fill out and submit the form, it invokes the function and sends the form details via email using SendGrid.

## Deployment Steps

I plan on updating this project to automate the deployment. For now, you can follow these steps to get this application up and running.

* Create an Azure Storage account. Enable [static website hosting](https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-static-website) and upload the **index.html** file from the **www** folder of this repo.
* [Create a SendGrid Account](https://docs.microsoft.com/en-us/azure/sendgrid-dotnet-how-to-send-email#create-a-sendgrid-account) in the Azure Portal
* Create an App Setting entry in your Function App called **SendGrid** that contains your SendGrid API key.
* Deploy the **ContactFormAPI** in this repo to your Function App using [VS Code](https://code.visualstudio.com/tutorials/functions-extension/getting-started).

## App Info

### Author

Mike Pfeiffer
[@mike_pfeiffer](https://twitter.com/mike_pfeiffer)

### Version

1.0.0

### License

This project is licensed under the Apache License 2.0

