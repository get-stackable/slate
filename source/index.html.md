---
title: Stackable API Reference

language_tabs:
  - javascript
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


# Learn the concepts

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

# API Endpoints

API Endpoints
Connect to stackable for restful endpoints.


GET /v1/containers

GET /v1/containers/:CONTAINER-ID

GET /v1/containers/:CONTAINER-ID/items

GET /v1/items

GET /v1/items/:ITEM-ID

POST /v1/items?containerId=CONTAINER-ID

PUT /v1/items/:ITEM-ID


# Authentication

We use a token based system to manage authentication. You will have access to two keys.

- **Public Keys** (ideal for reading data and sites that cannot use server side scripting)
- **Private Keys** (these provide a higher level of API access with advanced posting)

See the image below showing the key locations. --

# Obtaining a key

Each Stack will hold **containers** and will also have its own Public/Private Key. You can click the cog icon on the stack and you can then see your Keys.

If you like you can regenerate a key and also restrict what urls can access the data.

-- screen cap dashboard --

# Initialise libraries

Before using any of stackable's library, you need to initialise it

```javascript
var stackable = new Stackable('YOUR-STACK-KEY-HERE');
```

```php
$stackable = new Stackable('YOUR-STACK-KEY-HERE');
```

# GET all containers

```javascript
stackable.getContainers(function (error, result) {
    console.log(error, result);
});
```

```php
$result = $stackable->getContainers();
print_r($result);
```

```shell
# This is some shell code!
```

GET /v1/containers

Returns an array of all of your containers in stack.

# GET single container

```javascript
stackable.getContainer('CONTAINER-ID', function (error, result) {
    console.log(error, result);
});
```

```php
$result = $stackable->getContainer('CONTAINER-ID');
print_r($result);
```

```shell
# This is some shell code!
```

GET /v1/containers/:CONTAINER-ID

Returns an object of requested container in stack.

# GET container's all items

```javascript
stackable.getContainerItems('CONTAINER-ID', function (error, result) {
    console.log(error, result);
});
```

```php
$result = $stackable->getContainerItems('CONTAINER-ID');
print_r($result);
```

```shell
# This is some shell code!
```

GET /v1/containers/:CONTAINER-ID/items

Returns an array of items from requested container in stack.

### Optional Query Parameters

$limit=number

$skip=number

# GET stack's all items

```javascript
stackable.getAllItems(function (error, result) {
    console.log(error, result);
});
```

```php
$result = $stackable->getAllItems();
print_r($result);
```

```shell
# This is some shell code!
```

GET /v1/items

Returns an array of all items in stack (from all containers).

### Optional Query Parameters

$limit=number

$skip=number

# GET single items

```javascript
stackable.getItem('ITEM-ID', function (error, result) {
    console.log(error, result);
});
```

```php
$result = $stackable->getItem('ITEM-ID');
print_r($result);
```

```shell
# This is some shell code!
```

GET /v1/items/:ITEM-ID

Returns an object of single requested item.

# CREATE item

```javascript
var dataToPost = {
    name: 'John Doe',
    age: 29
};

stackable.createItem('CONTAINER-ID', dataToPost, function (error, result) {
    console.log(error, result);
});
```

```php
var dataToPost = [
    name => 'John Doe',
    age => 29
];

$result = $stackable->createItem('CONTAINER-ID', dataToPost);
print_r($result);
```

```shell
# This is some shell code!
```

POST /v1/items?containerId=CONTAINER-ID

Creates an item in requested container.

# UPDATE item

```javascript
var dataToUpdate = {
    name: 'John Doe',
    age: 29
};

stackable.updateItem('ITEM-ID', dataToUpdate, function (error, result) {
    console.log(error, result);
});
```

```php
var dataToPost = [
    name => 'John Doe',
    age => 29
];

$result = $stackable->updateItem('ITEM-ID', dataToPost);
print_r($result);
```

```shell
# This is some shell code!
```

PUT /v1/items/:ITEM-ID

Updates an requested item.


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

# API Examples

-- parminder do example of request and response here!!
