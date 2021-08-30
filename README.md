# Data Extension Helper in Cloud Pages

This is a helper to find Data Extensions faster. Trying to find in Marketing Cloud may be slow

![Page](./Data%20Extension%20Info%20Page.png)

:warning::warning::warning:

This page is hosted in a Cloud Page, so it is free accessible to anyone that has the link. **This Code doesn't make any authentication, but also doesn't retrieve Data Extension data (rows)**. 

The Data Extension links leads to [Query Studio](https://appexchange.salesforce.com/appxListingDetail?listingId=a0N3A00000FP3yFUAT), <ins>there is possible to access and manipulate Data Extension and it's rows. But in Query Studio Data Extension it is required Authentication (so it's secure)</ins>.

:warning::warning::warning:

## What you need to do?
1. [Create a CodeSnippet with the SSJS Code](#create-a-codesnippet-with-the-ssjs-code)
2. [Insert Backend in a Cloud Page Code Resource](#insert-backend-in-a-cloud-page-code-resource)
3. [Insert Frontend in a Cloud Page Landing Page changing URLs](#insert-frontend-in-a-cloud-page-landing-page-changing-urls)
4. Access the URL from Marketing Cloud where is your Frontend

## Create a CodeSnippet with the SSJS Code

Access Content Builder 

![Code Resource](./Access-Content-Builder.png)

Create a Code Snippet

![Code Snippet](./Create-Code-Snippet.png)

Insert the code [CodeSnippet.js](./CodeSnippet.js) and save it

After saving it, close and access again to find the Content ID

![Code ID](./Code%20Snippet%20ID.png)

Save this ID

## Insert Backend in a Cloud Page Code Resource
 
Create a new Code Resource in Marketing Cloud

![Code Resource](./Create%20Code%20Resource.png)

Copy the code [Backend.html](./Backend.html) and paste in the Code Resource you've just created

Replace the `<Created_CodeSnippet.js_ContentID>` with the Code ID from the Content you've created previously

![Insert Code ID](./Replace%20with%20Code%20ID.png)

Publish the page and save the URL

![Backend URL](./Backend-URL.png)

## Insert Frontend in a Cloud Page Landing Page changing URLs

Create a new Landing Page in Marketing Cloud

![Landing Page](./Create%20Landing%20Page.png)

Access the Code View, and replace all code html tag code with the code in [Frontend.html](./Frontend.html)

![Code View](./Access-Code-View.png)

Replace the `BASE_URL` and `BACKEND_ENDPOINT` with the URL from your backend

```javascript
const BASE_URL = 'https://yousubdomain.yourdomain.com';
const BACKEND_ENDPOINT = '/3iujpvyyab0';
```

## Access the URL from Marketing Cloud where is your Frontend

Access in your Browser

## Notes

It's just a fast helper, it needs improvements. Things that I

- [ ] Select Business Unit
- [ ] Open and Close Folder
- [ ] Add a Search Box
- [ ] Adjust layout