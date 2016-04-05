---
title: Stackable API Reference

language_tabs:
  - nodejs
  - php
  - shell

toc_footers:
  - <a href='http://www.stackable.space/'>Sign Up for a Developer Key</a>

includes:
  - errors

search: true
---

# Introduction

Welcome to the Stackable documentation. Stackable allows you to model content for websites & apps easily and have this available through a secure modern API. All data is returned in JSON including errors.

Along side detailed instructions on how to use our library we have provided boilerplates in various languages for you to examine and use in your next projects. Check out github Here.


# Learn the simple stackable concepts

**What is a Stack?**

Imagine a stack as holding all the data for  your website, App or Service it can hold many different types of data which you will model later as described below.

For instance if you create a stack called TODO APP inside it you can create containers maybe to hold TODO items, manage categories.

**What is a Container**

So the Stack holds your data, what you need to do is stack this data together in the real world we may stack together containers which hold items. Same principle in Stackable.

So a container is the type of data you wish to store, it may be products, blog posts, todo items, Users essentially you can create a container and using our drag and drop menu. These then belong to your Stack.

**How do i add Content?**

Once you have created your container you will see a preview of how the form may look. When you are hapy you can save this and then click manage items on the container menu. Here you will see an elegant dashboard with a familar way to enter data. You can share this with others eg content editors.


**So to summarise here is how you can imagine your who project.**

Stack: Your App or Website

Container: The Products or Blog posts you want to store

Item: A single item (post, product) that now lives in your container.

# API ENDPOINTS

API Endpoints
Connect to stackable for restful endpoints.


GET /v1/:container

GET /v1/:item

GET /v1/container/item

__ PARMINDER PUT ALL ENDPOINT REQUESTS HERE --

# Authentication

We use a token based system to manage authentication. You will have access to two keys.

- **Public Keys** (ideal for reading data and sites that cannot use server side scripting)
- **Private Keys** (these provide a higher level of API access with advanced posting)

See the image below showing the key locations. --

# Obtaining a key from a Stack

Each Stack will hold **containers** and will also have its own Public/Private Key. You can click the cog icon on the stack and you can then see your Keys.

If you like you can regenerate a key and also restrict what urls can access the data.

-- screen cap dashboard --

# API EXAMPLES

-- parminder do example of request and response here!!

# GET content

GET /v1/containers

Returns an array of all of your containers objects.

Optional Query Parameters

limit=number
skip=number

# PUT content

PUT /v1/containers


# Let make something

Stackable has client libraries to help you easily manage content on your website or app. Check out these examples below.

A basic example

Browser

Add the stackable.min.js file from the Official Stackable JavaScript Client on GitHub to your app.

**Below is a real world example Using JAVASCRIPT**

---- PARMINDER ---

```nodejs
here is an example of using the private and public keys with a nodejs app.
```

Install the Official Stackable JavaScript Client on NPM.

-- PARMINDER ---

```php
here is an example of using the private and public keys with a nodejs app.
```

-- PARMINDER --
