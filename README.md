<p align="left">
  <img width="300" src="https://camo.githubusercontent.com/e5871e45b0178db73800a382be64a031c65b195eddecccf95f49d8a7f5f6c481/68747470733a2f2f6b6f6e74656e626173652e636f6d2f5f6e6578742f7374617469632f6d656469612f6b6f6e74656e626173652d6c6f676f2d6c696768742e66616564323864652e737667">
</p>
 
<a href="https://app.kontenbase.com/"><img alt="App" src="https://img.shields.io/badge/Visit-Kontenbase-orange" /></a>

<details>
    <summary>
        Table of Content
    </summary>

<!-- TOC -->

- [Getting Started](#getting-started)
    - [Introduction](#introduction)
    - [Features](#features)
    - [Quickstart Guide](#quickstart-guide)
        - [Create Workspace](#create-workspace)
        - [Create Service](#create-service)
        - [Customize Fields](#customize-fields)
        - [Auth](#auth)
        - [Try Service](#try-service)
            - [POST](#post)
            - [GET](#get)
            - [PATCH](#patch)
            - [DELETE](#delete)
- [Overview](#overview)
    - [Creating Workspace](#creating-workspace)
    - [Creating Public Service](#creating-public-service)
    - [Data Modeling](#data-modeling)
    - [Try Service](#try-service)
        - [GET](#get)
        - [POST](#post)
        - [PATCH](#patch)
        - [DELETE](#delete)
    - [Creating Private Service](#creating-private-service)
    - [Authentication](#authentication)
        - [Register](#register)
        - [Login](#login)
        - [Logout](#logout)
    - [Authorization](#authorization)
    - [API KEY](#api-key)
        - [API KEY Usage](#api-key-usage)
        - [Generate New API KEY](#generate-new-api-key)
        - [Delete Workspace](#delete-workspace)
- [API](#api)
    - [Basic Service](#basic-service)
        - [GET](#get)
            - [Filter](#filter)
            - [Sort](#sort)
            - [Limit](#limit)
        - [POST](#post)
        - [PATCH](#patch)
        - [DELETE](#delete)
    - [Storage  File Upload](#storage--file-upload)
        - [GET](#get)
        - [POST](#post)
        - [PATCH](#patch)
        - [DELETE](#delete)
    - [Authentication](#authentication)
        - [Register](#register)
        - [Login](#login)
        - [Logout](#logout)
- [SDK](#sdk)
    - [Basic Service](#basic-service)
        - [Find](#find)
            - [Filter](#filter)
            - [Sort](#sort)
            - [Limit](#limit)
            - [FindById](#findbyid)
        - [Create](#create)
        - [Update](#update)
        - [Delete](#delete)
    - [Storage  File Upload](#storage--file-upload)
        - [Upload](#upload)
        - [Delete](#delete)
    - [Authentication](#authentication)
        - [Register](#register)
        - [Login](#login)
        - [Logout](#logout)
- [Web Socket](#web-socket)
    - [Setup](#setup)
    - [Trigger](#trigger)
    - [Listen](#listen)
- [Example Projects](#example-projects)
    - [Todo](#todo)
        - [Getting Started](#getting-started)
            - [Kontenbase Back-end Setup](#kontenbase-back-end-setup)
            - [Front-end Setup](#front-end-setup)
    - [Blog](#blog)
        - [Getting Started](#getting-started)
            - [Kontenbase Back-end Setup](#kontenbase-back-end-setup)
            - [Front-end Setup](#front-end-setup)
    - [Chat](#chat)
        - [Getting Started](#getting-started)
            - [Kontenbase Back-end Setup](#kontenbase-back-end-setup)
            - [Front-end Setup](#front-end-setup)

<!-- /TOC -->

</details>

# Getting Started

## Introduction
> No code Backend API, Fast and Easy!

Kontenbase is a Backend as service that easily create backend API, auth, and storage in less than 1 minute without coding.

Kontenbase is focused on enabling developers (especially front-end developers) to build back-end API (currently focuse on REST API) without having to touch backend code at all.

But of course, it's still possible to create a custom backend service too.

## Features
Kontenbase let you focus on the Frontend & Product.

- [x] Hosted Backend
- [x] Auto Generated API & SDK
- [x] Hosted Database
- [x] Database Migration
- [x] Authentication and Authorization
- [x] Realtime subscriptions
- [x] Storage
- [ ] Functions (coming soon)
- [ ] Internal Tools (coming soon)

## Quickstart Guide
This quickstart guide is aimed to help new user to build backend API using Kontenbase. Starting by creating a workspace, creating service with its fields and try the service. To get started, you need to log in with your google account.

### Create Workspace
After logging in, this page will be displayed 

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/kTxStNJUyifjNcV/1.png">
</p>

Enter your workspace name then click `Continue` to start creating services.

### Create Service
The project has neither data nor services. All you have to do is create your first service. Two buttons are provided to create the first service. Top left  button or center of page button. Any of them is fine.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/rCgjlzRQVdVfSRb/2.png">
</p>

For this quickstart guide, we will make simple `blogs` application as a **Private Service**.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/gkmLoQRlRLyAojO/1.png">
</p>

We will talk about the difference between *public* and *private* service later.

### Customize Fields
Click the `Customize Fields` button to expand the service details and display two automatic fields. 

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/csImaqMzqfGuVtH/2.png">
</p>

When configuring the service, make sure that the field types are properly organized according to your project needs. To edit or delete a field, click the field to see options.

Create some fields by clicking `Add New` button.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/uCiMOiizHtCnldk/3.png">
</p>

Only 1 minute and you had created your service and its fields, auth, and storage. Let's start to try your service!

### Auth
Authentication will check who you are and authorization will check what you can do.

- Public
    <p align="left">
  	<img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/grdgTKDtyuLuWHe/3.png">
    </p>

- Authenticated
    <p align="left">
  	<img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/IOcwzWXYXMQsslq/4.png">
    </p>

### Try Service

<p align="center">
  <img width="400" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/cbXdfgIEEPEGcPd/1.png">
</p>

Each try service displays the API of the service. You may try your service directly on Kontenbase, or copy the API and try the service on any API testing platform.

Let's begin to try service on Kontenbase!

#### POST
Expand the service and select `Create Record` to try POST API. Try content entry using the ***simple*** method.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/LYMKPoGnFYxsXmr/1.png">
</p>

Oops, an error response : `Unauthorized` . It looks we should register a user to access the service.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/wczqXXbvgweNxSS/2.png">
</p>

You get a token but we will pass it for now because we will use *simple* method. Go back to create record.

Don't forget to choose authenticated as bar with the user we recently added.
<p align="center">
  <img width="400" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/SRuhjyNplbrztDT/1.png">
</p>

Entry record.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/heRcChpHvQfghYV/3.png">
</p>

The detail response :

````json
{
    "_id": "61d3f0a02a43d87ac4519e3b",
    "content": "Coming soon",
    "coverImage": [
        {
            "fileName": "score.png",
            "url": "https://api.kontenbase.com/upload/file/61d3ea682a43d87ac4519dfb/GYymOvcgIXtmyjJ/score.png"
        }
    ],
    "createdBy": "61d3f0361836652ed60c8b0c",
    "date": "2022-01-04",
    "title": "How to get good score?"
}
````

From the response, the detail response let us know that the service also has storage to store the record. That's way the action to upload file is succeed.

#### GET
Still on simple method, Find Records by clicking `Send` in Find Records section.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/TQKVYCFeWPLmNhR/4.png">
</p>

Your records are shown in response box, this is the detail records of blogs service.

````json
[
    {
        "_id": "61d3f0a02a43d87ac4519e3b",
        "title": "How to get good score?",
        "content": "Coming soon",
        "date": "2021-01-04",
        "coverImage": [
            {
                "fileName": "score.png",
                "url": "https://api.kontenbase.com/upload/file/61d3ea682a43d87ac4519dfb/GYymOvcgIXtmyjJ/score.png"
            }
        ]
    }
]
````

#### PATCH
You need the ID of the records in order to update record. Copy and paste the ID into the box. Then enter your up-to-date record.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/aGOUmxzfIIzNlkD/2.png">
</p>

When you navigate back to Find records, current find record detail is below.

````json
[
    {
        "_id": "61d3f0a02a43d87ac4519e3b",
        "title": "History of Java",
        "content": "Coming soon",
        "date": "2022-01-04",
        "coverImage": [
            {
                "fileName": "java.png",
                "url": "https://api.kontenbase.com/upload/file/61d2b3a02a43d87ac4519d2d/QUDGJqxKWYqbhOW/java.png"
            }
        ]
    }
]
````

#### DELETE
Just like the usual way in your API testing platform. You need the ID of the record to Delete Record.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/rQBtjbosOyvFjPA/7.png">
</p>

Easy, right?

# Overview

## Creating Workspace
<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/kTxStNJUyifjNcV/1.png">
</p>

Upon login, this is the beginning. Create workspace where the project development environment will be happened.

## Creating Public Service
A service is place to manage and store records based on the field arrangement. There are 2 types of service on Kontenbase : Public Service and Private Service.

In Public Service, users are free to search, create, update, and even delete records without being authenticated.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/ofpgWDRdOQJvpiG/3.png">
</p>

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/uTQSGcfgfwsaUKX/7.png">
</p>

## Data Modeling
Users have freedom to choose the data modeling of each field according to their app needs and it will generated a backend like the chosen type. 

Both fields ( name and notes ) are default fields that can be edited or deleted. Click the field and you will be shown the options.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/GbHndVpzNGrrWvu/1.png">
</p>

Add more fields based on the app needs.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/GMmJePraueBDDrz/9.png">
</p>

|Data Type|Usage |Additional Feature|
|---------|------|------------------|
|Link to Record|Use `Link to Record` type to make relationship, where users can get results that combine record from different service.|Linking to multiple record|
|Single Line Text|A `single line text` is a single textbox use for collecting short phrase up to 255 characters. This is data type is used when you need to enter username, paassword, title, and so on.|Default Value|
|Long Text|`Long Text` Type commonly shaped as textarea, usually used for many sentences.||
|Attachment| Storage [Upload File] as array of object||
|Checkbox|A `checkbox` also can be called *boolean* because it has the value checked for true or unchecked for false. Such as to show whether you have finished any task or not. You can use checkbox.|Style|
|Multiple Select| Array of object|Add options|
|Single Select| Object|Add options|
|Date |Date|Include a time field|
|Phone Number |String||
|Email|String||
|Url|String||
|Number|You may use integer or decimal data type. The detail arrangement of integer or decimal are inside `number` data type.| Allow negative number & Default Value
|Currency | Integer | Currency symbol, Precision, Allow negative number, Default value|
|Percent |Integer | Precision & Default Value|
|Duration | Time | Duration format|
|Rating |Integer | Max & Style|
|Created At |Timestamp||
|Updated At |Timestamp||
|Created By |Object||
|Updated By |Object||

## Try Service
Each service generated is able to try right away. The basic functions are :

### GET
List of records each service.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/GKDexQjwGPXqjHA/11.png">
</p>

The records are shown on response box, this is the detail record of blogs service.

````json
[
    {
        "_id": "61d2c3162a43d87ac4519d5e",
        "title": "Welcome 2022: New Year preparation !",
        "content": "TBD",
        "date": "2021-12-31",
        "coverImage": [
            {
                "fileName": "todo.png",
                "url": "https://api.kontenbase.com/upload/file/61c3cfc52a43d87ac4519085/uOSPAqgOfvSpaQG/todo.png"
            }
        ]
    }
]
````

### POST
Content entry.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/ydEiGCQrhOlhqxG/10.png">
</p>

### PATCH
Update record.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/UxlhmrieqbDNhCB/12.png">
</p>

### DELETE
Delete record.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/nzukIrtBXaeEeLK/13.png">
</p>

## Creating Private Service
In Private Service, users need to be authenticated in order to access the service. 

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/IYKYlgmLzfNuMxo/c.png">
</p>

It has two additional services : authentication and users, when you create private service.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/itWYkAKudECxops/d.png">
</p>

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/ytHOSezyoatbgBT/e.png">
</p>

The Users services is a private service as well.

## Authentication
Access control for each service especially private service. Authentication find out who you are and the authorization will take place. 

### Register
To Register as User and return a token for enabling access control based on authorization.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/IsrBSiSkzjpdqpv/1.png">
</p>

**Noted** : First registered user will be an admin.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/jLctveVjOqpjtyC/2.png">
</p>

```json
{
    "token": "a9c7746c5b550098357f456836630c51"
}
```

### Login
Login with an existing user account and return a token for enabling access control based on authorization.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/TnwmxxKElPdgSMq/3.png">
</p>

````json
{
    "token": "abe68fba36335a70493b37c46d46c7d9"
}
````

### Logout
End the authentication session.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/pfggcUxmlSEcxQr/4.png">
</p>

## Authorization
Navigate to the authorization button. Authorization will shows any allowed access control when authenticating as public/authenticated/admin in each service. Users are free to change the permissions and rules as well.

**Public Service ( for example : blogs)**

- Authenticating as **Public**
<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/TtYrSnLfGgzDnsV/a.png">
</p>

  - Authenticating as **Authenticated**
<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/TboRyjaQCrxRQLQ/b.png">
</p>

**Private Service ( for example : comments )**

  - Authenticating as **Public**

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/bapnufHcxwBWFhr/f.png">
</p>

  - Authenticating as **Authenticated**
<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/WAzbRxOCpmFPFqP/g.png">
</p>

## API KEY

### API KEY Usage
The API KEY is a unique identifier used to identify and authenticate an application or user. It calls the relates APIs that store the application schema, auth, and record/storage.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/IOntAXYqaxFEuzE/1.png">
</p>

### Generate New API KEY
Why do wee need to generate New API KEY?
- Uncontrolled API calls
- Potentially malicious activity
- so on.

If they really happened, using this button will generate a new API KEY.

<p align="left">
  <img width="700" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/vDfOwWeUYgVLiHa/2.png">
</p>

### Delete Workspace
Delete workspace means delete the API KEY. The API KEY will no longer exist along with the the related APIs that store the records.

# API
API used as interface between the computers programme and currently we support REST API. The API naming convention on Kontenbase just like this :

`HTTP_Url`+`API_KEY`+`/`+`Service_Name`

e.g. https://api.kontenbase.com/query/api/v1/f4b4745a-84d4-49da-ae24-0d399ca387e2/blogs

Special case for auth, the API naming convention is :

`HTTP_Url`+`API_KEY`+`/`+`Auth_Process`

e.g. https://api.kontenbase.com/query/api/v1/f4b4745a-84d4-49da-ae24-0d399ca387e2/register

Easier way? Directly copy on the top bar of each method service.

## Basic Service
### GET
You can find record not in simple way. Ya, using some parameter/condition that will make your records readable based on what you need. 

For example, we will access blogs service.
#### Filter
Available condition : equal, not equal, contains, not contains

<p align="left">
  <img width="600" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/wfsapDaNSpDwVMe/filter.png">
</p>

````json
[GET]
API_Url/service_name
Need Developer Assitant
````
#### Sort
Available sort : Ascending and Descending

<p align="left">
  <img width="600" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/nwFAhCzCHQGhmeW/sort.png">
</p>

````json
[GET]
API_Url/service_name
Need Developer Assitant
````

#### Limit
- Limit : Used to give maximum records that will be shwon
- Skip : skip/pass record

<p align="left">
  <img width="600" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/dYKUDFQzlqHlvDK/limit.png">
</p>

````json
[GET]
API_Url/service_name
Need Developer Assitant
````

### POST
To create record.

````json
[POST]
API_Url/service_name

body : {
  "name" : "Youth"
}

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

### PATCH
To update record.

````json
[PATCH]
API_Url/service_name/id

body : {
  "name" : "We go up"
}

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

### DELETE
To remove record.

````json
[POST]
API_Url/service_name/id

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

## Storage ( File Upload )
File upload reflect the Basic Service. In order to file upload, you need field type `attachment`.
### GET
To find record.

````json
[GET]
API_Url/service_name
````

### POST
To upload the file.

<p align="left">
  <img width="600" src="https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/ggqJxvjEmRmUElu/file.png">
</p>

````json
[POST]
API_Url/service_name

body : {
  "titile" : "Hello",
  "content" : "Coming soon",
  "coverImage": [
        {
            "fileName": "hi.png",
            "url": "https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/nwFAhCzCHQGhmeW/hi.png"
        }
    ],
    "date": "2022-01-04"
}

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

### PATCH
To update record.

````json
[PATCH]
API_Url/service_name/id

body : {
  "name" : "Youth"
}

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

### DELETE
To remove record.

````json
[POST]
API_Url/service_name/id

Header: {
  "Authorization": "Bearer YourGeneratedTokenHERE"
}
````

You need fill the token when occured in private service.

## Authentication

### Register
To register a user and return token to access the service based on authorization.

````json
[POST]
API_Url/register

body: {
  "firstName": "Someone",
  "email" : "someone@gmail.com",
  "password" : "secrete"
}
````

### Login
To login as user that has been registered and return token to access the service based on authorization.

````json
[POST]
API_Url/login

body: {
  "email" : "someone@gmail.com",
  "password" : "secrete"
}
````

### Logout
To end the authentication session.

````json
[POST]
API_Url/logout
````

# SDK

## Basic Service

### Find

#### Filter

#### Sort

#### Limit

#### FindById

### Create

### Update

### Delete

## Storage ( File Upload )

### Upload

### Delete

## Authentication

### Register

### Login

### Logout

# Web Socket

## Setup

## Trigger

## Listen

# Example Projects
These are some projects we had prepared. Simply clone [the frontend repository](https://github.com/kontenbase/kontenbase.git) for these project.

## Todo
![Kontenbase](https://user-images.githubusercontent.com/2161622/147661746-f532af50-7e67-465d-a88c-56fd4866a559.png)

Simple Todo App example with Next JS as Front-end, and Kontenbase as Back-end

<a href="https://kontenbase-todo.vercel.app"><img alt="App" src="https://img.shields.io/badge/Live Demo-Todo-blue" /></a>

### Getting Started
Make sure you already installed latest NodeJS on your PC.

#### Kontenbase Back-end Setup
1. Create Account/Login to your [Kontenbase](www.kontenbase.com. "Kontenbase")
2. Create **todos** as a *private service*
3. Customize fields
	- name : Single Line Text
	- checked : check box
	![](https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/KphaGoGvArawPVH/5.png)

4. Copy the API KEY from the workspace Settings

#### Front-end Setup
Run the Front-end development server:

1. Navigate the directory to /nextjs-todo and install the dependencies with : `npm install`
2. Create a file .env copy from .env.example
3. Change the NEXT_APP_KONTENBASE_API_KEY you get in the Kontenbase
4. Start developing and watch for code changes : `npm run dev`
Open http://localhost:3000 with your browser to see the result.

## Blog
![Kontenbase](https://camo.githubusercontent.com/30ac71a7980b36dd9c6ff4a7166049130586369bb59bb713d2b47fa35b7663da/68747470733a2f2f6b6f6e74656e626173652d626c6f672e76657263656c2e6170702f6c6f676f2e737667)

Simple Blog example with Next JS as Front-end, and Kontenbase as Back-end

<a href="https://kontenbase-blog.vercel.app"><img alt="App" src="https://img.shields.io/badge/Live Demo-Blog-orange" /></a>

### Getting Started
Make sure you already installed latest NodeJS on your PC.

#### Kontenbase Back-end Setup
1. Create Account/Login to your [Kontenbase](www.kontenbase.com. "Kontenbase")
2. Create **blogs** as a *private service*
3. Customize fields
	- title : Single Line Text
	- content : Long Text
	- slug : Single Line Text
	- date : Created At
	- coverImage : Url
	- author : Created By
	- excerpt : Long Text
	![](https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/BWJGXJqnYkFthKC/6.png)

4. Copy the API KEY from the workspace Settings

#### Front-end Setup
Run the Front-end development server:

1. Navigate the directory to /nextjs-blog and install the dependencies with : `npm install`
2. Create a file .env copy from .env.example
3. Change the NEXT_APP_KONTENBASE_API_KEY you get in the Kontenbase
4. Start developing and watch for code changes : `npm run dev`
Open http://localhost:3000 with your browser to see the result.

## Chat
![Kontenbase](https://user-images.githubusercontent.com/2161622/147641752-a059d073-3acc-472f-844e-f9d4553e4c50.png)

Simple Chat App example with React JS as Front-end, and Kontenbase as Back-end

<a href="https://kontenbase-chat.vercel.app"><img alt="App" src="https://img.shields.io/badge/Live Demo-Chat-green" /></a>

### Getting Started
Make sure you already installed latest NodeJS on your PC.

#### Kontenbase Back-end Setup
1. Create Account/Login to your [Kontenbase](www.kontenbase.com. "Kontenbase")
2. Create **chats** as a *private service*
3. Customize fields
	- name : Single Line Text
	- createdBy : Created By
	- createdAt : Created At
	![](https://api.kontenbase.com/upload/file/61d2ad972a43d87ac4519cff/LlCTtDHIJcazqPJ/7.png)

4. Copy the API KEY from the workspace Settings

#### Front-end Setup
Run the Front-end development server:

1. Navigate the directory to /reacttjs-chat and install the dependencies with : `npm install`
2. Create a file .env copy from .env.example
3. Change the NEXT_APP_KONTENBASE_API_KEY you get in the Kontenbase
4. Start developing and watch for code changes : `npm run start`
Open http://localhost:3000 with your browser to see the result.
