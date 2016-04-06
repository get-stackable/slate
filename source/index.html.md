---
title: Stackable API Reference

language_tabs:
  - javascript
  - php
  - shell

toc_footers:
  - <a href='http://www.stackable.space/'>Sign Up for a Developer Key</a>

includes:
  - authentication
  - apiUsage
  - letMakeSomething
  - errors
  - apiExamples

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
