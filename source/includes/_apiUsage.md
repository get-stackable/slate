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
