# Data Extension Helper in Cloud Pages

This is a helper to find Data Extensions faster. Trying to find in Marketing Cloud may be slow

![Page](https://user-images.githubusercontent.com/26888271/131375620-e2d71b51-a7d3-441b-ad3b-0e72f07df9b9.png)

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

![Content Builder](https://user-images.githubusercontent.com/26888271/131375627-c6298ea1-e87e-442b-9603-451dfab66ba8.png)

Create a Code Snippet

![Create Code Snippet](https://user-images.githubusercontent.com/26888271/131377054-26ffc412-fa72-4557-86dd-449a4aa52ee7.png)

Insert the code [CodeSnippet.js](./CodeSnippet.js) and save it

After saving it, close and access again to find the Content ID

![Code Snippet ID](https://user-images.githubusercontent.com/26888271/131375634-eff56a0c-59da-4339-b228-419eeb110ba6.png)

Save this ID

## Insert Backend in a Cloud Page Code Resource
 
Create a new Code Resource in Marketing Cloud

![Code Resource](https://user-images.githubusercontent.com/26888271/131375593-62b7499c-10bd-4a0c-8b0c-04a9e7920c31.png)

Copy the code [Backend.html](./Backend.html) and paste in the Code Resource you've just created

Replace the `<Created_CodeSnippet.js_ContentID>` with the Code ID from the Content you've created previously

![Insert Code ID](https://user-images.githubusercontent.com/26888271/131375623-bbed7d92-1f80-4418-8c19-63716a66ba5e.png)

Publish the page and save the URL

![Backend URL](https://user-images.githubusercontent.com/26888271/131375630-e3a47961-ca45-4282-9a5b-402f3773bc08.png)

## Insert Frontend in a Cloud Page Landing Page changing URLs

Create a new Landing Page in Marketing Cloud

![Landing Page](https://user-images.githubusercontent.com/26888271/131375625-e6fbcf69-4f08-4203-b63a-6e10f91ae806.png)

Access the Code View, and replace all code html tag code with the code in [Frontend.html](./Frontend.html)

![Code View](https://user-images.githubusercontent.com/26888271/131375616-a49725c7-7b1d-4f38-82ff-b64ff3503eab.png)

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
