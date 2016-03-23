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

  
# Authentication  

We use a token based system to manage authentication. You will have access to two keys.

- **Public Keys** (ideal for reading data and sites that cannot use server side scripting)
- **Private Keys** (these provide a higher level of API access with advanced posting)

See the image below showing the key locations.

# Obtaining a key from a Stack

Imagine a stack as your app or website. When you login you can create a Stack.   
  
Each Stack will hold **containers** and will also have its own Public/Private Key. You can click the cog icon on the stack and you can then see your Keys.  
  
If you like you can regenerate a key and also restrict what urls can access the data.

```nodejs
here is an example of using the private and public keys with a nodejs app.
```

Watch a video here.

# Stacks

As we discussed earlier Stacks are simliar to your whole app. For instance if you create a stack called TODO APP inside it you can create containers maybe to hold TODO items, manage categories.

Below we will show you how to grab the content in every container that exists in your stack

> List All containers

```nodejs
code here to list all containers
```

```php
PHP list all containers
```

```shell
List all containers
```

> Make sure to replace `public key` with your API key.


# Containers

Containers are the heart of your data. Once hyou have clicked on a new setack you can then click the container button as show here.

You can now create a new container.

- Drag and Drop field elements on the page
- Create validations on the fields
- Preview how the fields look.

### list containers items

This code shows you how to read from a specific container

```nodejs
read container
```



## Get All containers

```nodejs
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get
```

```php
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get()
```

```shell
curl "http://example.com/api/kittens"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
[
  {
    "id": 1,
    "name": "Fluffums",
    "breed": "calico",
    "fluffiness": 6,
    "cuteness": 7
  },
  {
    "id": 2,
    "name": "Max",
    "breed": "unknown",
    "fluffiness": 5,
    "cuteness": 10
  }
]
```

This endpoint retrieves all kittens.



### Query Parameters

Parameter | Default | Description
--------- | ------- | -----------
include_cats | false | If set to true, the result will also include cats.
available | true | If set to false, the result will include kittens that have already been adopted.

<aside class="success">
Remember — a happy kitten is an authenticated kitten!
</aside>

## Get a Id

```ruby
require 'kittn'

api = Kittn::APIClient.authorize!('meowmeowmeow')
api.kittens.get(2)
```

```python
import kittn

api = kittn.authorize('meowmeowmeow')
api.kittens.get(2)
```

```shell
curl "http://example.com/api/kittens/2"
  -H "Authorization: meowmeowmeow"
```

> The above command returns JSON structured like this:

```json
{
  "id": 2,
  "name": "Max",
  "breed": "unknown",
  "fluffiness": 5,
  "cuteness": 10
}
```

This endpoint retrieves a specific kitten.

<aside class="warning">Inside HTML code blocks like this one, you can't use Markdown, so use <code>&lt;code&gt;</code> blocks to denote code.</aside>

### HTTP Request

`GET http://example.com/kittens/<ID>`

### URL Parameters

Parameter | Description
--------- | -----------
ID | The ID of the kitten to retrieve

