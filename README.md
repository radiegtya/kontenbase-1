<p align="left">
  <img width="300" src="https://camo.githubusercontent.com/e5871e45b0178db73800a382be64a031c65b195eddecccf95f49d8a7f5f6c481/68747470733a2f2f6b6f6e74656e626173652e636f6d2f5f6e6578742f7374617469632f6d656469612f6b6f6e74656e626173652d6c6f676f2d6c696768742e66616564323864652e737667">
</p>
 
# Getting Started

## Introduction
> No code Backend API, Fast and Easy!

Kontenbase is a Backend as service that easily create backend API, auth, and storage in less than 1 minute without coding.

Think of it as a very simple alternative of:
- JSON Placeholder
- Postman
- Strapi
- Firebase
- Supabase
- and other API-focused tools

Kontenbase is focused on enabling developers (especially front-end developers) to build back-end API (currently focused on REST API) without having to touch backend code at all.

But of course, it's still possible to create a custom backend service too.

### Features
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
This quickstart guide is aimed to help new User to build backend API using Kontenbase. Starting by creating a workspace, creating service with its fields, try the service. To get started, you need to [log in](app.kontenbase.com) with your google account.

### Create Workspace
After logging in, this page will be displayed 

<p align="left">
  <img width="700" src="workspace">
</p>

Enter your workspace name then click `Continue` to start creating services.

### Create Service
The project has neither data nor services. All you have to do is create your first service. Two buttons are provided to create the first service. Top right button or center of page button. Any of them is fine.

<p align="left">
  <img width="700" src="empty service">
</p>

For this quickstart guide, we will make simple `todos` application using a **Private Service**.

<p align="left">
  <img width="700" src="nama todos">
</p>

We will talk about the difference between *public* and *private* service later.

### Customize Fields
Click the `Customize Fields` button to expand the service details and display two automatic fields. 

<p align="left">
  <img width="700" src="auto field">
</p>

When configuring the service, make sure that the field types are properly organized according to your project needs. To edit or delete a field, click the field to see options.

<p align="left">
  <img width="700" src="edit and delete">
</p>

Create some fields by clicking `Add New` button.

<p align="left">
  <img width="700" src="fields">
</p>

Only 1 minute and you had created your service and its fields, auth, and storage. Let's start to try your service!

### Auth
Authorization section will check who you are and authorization will check what you can do.

<p align="left">
  <img width="700" src="authorization bar">
</p>

Navigate to the authorization button and yo will know any permissions of each role. Beside, there is also settings and search bar.

- Authenticating as Public
    <p align="left">
  	  <img width="700" src="public">
    </p>

- Authenticated
    <p align="left">
  	  <img width="700" src="authenticated">
    </p>

### Try Service

<p align="center">
  <img width="400" src="bar API">
</p>

Each try service displays the API of the service. You may try your service directly on Kontenbase, or copy the API and try the service on any API testing platform.

Let's begin to try service on Kontenbase!

#### POST
Expand the service and select `Create Record`. Try content entry using the ***simple*** method.

<p align="left">
  <img width="700" src="unauthorized">
</p>

Oops, an error response : `Unauthorized` . It looks we should register a user to access the service.

<p align="left">
  <img width="700" src="register">
</p>

You get a token as the response message from register reuqest. But we will pass it for now because we will use *simple* method. Navigate back to create record section.

Don't forget to choose `authenticated as bar` with the user we recently added.
<p align="center">
  <img width="400" src="bar authenticated">
</p>

Entry record.

<p align="left">
  <img width="700" src="entry record">
</p>

The detail response :

````json
detail response
````

From the response, we know that the service also has storage to store the record. That's way the post request is succeed.

Let's add more recordies, buddy!

### GET
Still on simple method GET section, there are some conditions displayed to find records: filter, sort, limit.

  - Filter 
    <p align="left">
      <img width="700" src="filter checked : true">
    </p>

    Response Message :

    ````json
    filter
    ````

  - Sort
    <p align="left">
      <img width="700" src="sort name ascending">
    </p>

    Response Message :

    ````json
    sort
    ````

  - Limit
    <p align="left">
      <img width="700" src="limit 2 skip 1">
    </p>

    Response Message :

    ````json
    limit
    ````
## Frontend Setup
We had setup the backend. Next,let's do the frontend part. In fact, you may choose any technologies the frontend part.

In case of consumed Kontenbase API on frontend, We had prepared a frontend using NextJS. Simply clone [here](github.com/kontenbase/kontenbase) and follow the instruction written there.

<p align="left">
  <img width="700" src="https://user-images.githubusercontent.com/2161622/147662051-f1311ebe-dc17-429e-b203-ceecaec2c3d5.png">
</p>

Then, let's discuss [Kontenbase SDK](https://www.npmjs.com/package/@kontenbase/sdk) implementation on the frontend.

### Usage
Configure package with your account's API key obtained from your Kontenbase Dashboard.

/lib/kontenbase.ts

```
import { KontenbaseClient } from '@kontenbase/sdk'

const kontenbase = new KontenbaseClient({
  apiKey: process.env.NEXT_PUBLIC_KONTENBASE_API_KEY || '',
})

```

This will direct you to your Kontenbase API KEY. So, you copy your API KEY from your app.

### Authentication
Use kontenbase auth services for manage your user.

#### Login
```
const { data } = await kontenbase.auth.login({
  email: 'user@gmail.com',
  password: 'password',
})
```

### Storage
#### Get
```
const { data } = await kontenbase.service('New Service').find()
```

For more detail explanation, you may visit Kontenbase SDK Documentation.

# Overview

## Creating Workspace
<p align="left">
  <img width="700" src="blank workspace">
</p>

Upon login, this is the beginning. Create workspace where the project development environment will be happened.

## Creating Public Service
A service is place to manage and store records based on the field arrangement. There are 2 types of service on Kontenbase : Public Service and Private Service.

In Public Service, users are free to search, create, update, and even delete records without being authenticated.

<p align="left">
  <img width="700" src="create public service belum disave">
</p>

<p align="left">
  <img width="700" src="exapand public service dgn fields">
</p>

## Data Modeling
Users have freedom to choose the data modeling of each field according to their app needs and it will generated a backend like the chosen type. 

Both fields ( name and notes ) are default fields that can be edited or deleted. Click the field and you will be shown the options.

<p align="left">
  <img width="700" src="edit and delete">
</p>

Add more fields based on the app needs. For example, the blogs app.. 

<p align="left">
  <img width="700" src="fields blogs">
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

### POST
Content entry.

<p align="left">
  <img width="700" src="post blogs">
</p>

````json
get
````

### GET
List of records each service.

<p align="left">
  <img width="700" src="get blogs">
</p>

The records are shown on response box, this is the detail record of blogs service.

````json
get
````

### PATCH
Update record.

<p align="left">
  <img width="700" src="patch ">
</p>

The records are shown on response box, this is the detail record of blogs service.

````json
get
````

### DELETE
Delete record.

<p align="left">
  <img width="700" src="delete">
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
```
const { data } = await kontenbase.service('New Service').find()
```

#### Filter
- Equal
```
const { data } = await kontenbase.service('New Service').find({ where: { name: 'John'} })
```

- not equal 
```
const { data } = await kontenbase.service('New Service').find({ where: { name: { $ne: 'John' } } })
```

- contains
```
const { data } = await kontenbase.service('New Service').find({ where: { name: { $contains: 'John' } } })
```

- not contains
```
const { data } = await kontenbase.service('New Service').find({ where: { name: { $notContains: 'John' } } })
```

- include
```
const { data } = await kontenbase.service('New Service').find({ where: { name: { $in: ['John'] } } })
```

- not include
```
const { data } = await kontenbase.service('New Service').find({ where: { name: { $nin: ['John'] } } })
```

- less than
```
const { data } = await kontenbase.service('New Service').find({ where: { total: { $lt: 10 } } })
```

- less than equal
```
const { data } = await kontenbase.service('New Service').find({ where: { total: { $lte: 10 } } })
```

- greater than
```
const { data } = await kontenbase.service('New Service').find({ where: { total: { $gt: 10 } } })
```

- greater than equal
```
const { data } = await kontenbase.service('New Service').find({ where: { total: { $gte: 10 } } })
```

#### Sort
```
const { data } = await kontenbase.service('New Service').find({ sort: { name: 1 } })
```

#### Limit
```
const { data } = await kontenbase.service('New Service').find({ limit: 10 })
```

#### FindById
```
const { data } = await kontenbase.service('New Service').getById("605a251d7b8678bf6811k3b1")
```

### Create
```
const { data } = await kontenbase.service('New Service').create({
  Name: 'Record',
  Notes: 'Hello world'
})
```

### Update
```
const { data } = await kontenbase.service('New Service').updateById("605a251d7b8678bf6811k3b1", {
  Name: 'New Record',
})
```

### Delete
```
const { data } = await kontenbase.service('New Service').deleteById("605a251d7b8678bf6811k3b1")
```

## Storage ( File Upload )

### Upload
```
const file = event.target.files[0]
const { data } = await kontenbase.storage.upload(file)
```

### Delete

## Authentication
Use kontenbase auth services for manage your user.

### Register
```
const { data } = await kontenbase.auth.register({
  firstName: 'John',
  lastName: 'Doe',
  email: 'user@gmail.com',
  password: 'password',
})
```

### Login
```
const { data } = await kontenbase.auth.login({
  email: 'user@gmail.com',
  password: 'password',
})
```

### Logout
```
const { data } = await kontenbase.auth.logout()
```

# Web Socket

## Setup

## Trigger
```
kontenbase.realtime.subscribe('New Service', (message) => {
  console.log(message)
})
```

## Listen
```
const key = await kontenbase.realtime.subscribe('New Service', (message) => {
  console.log(message)
})

kontenabase.unsubscribe(key)
```

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
