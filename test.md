# CRUOD - CRUD in full, Create, Read, Update, Overwrite, Delete

## POST
### The use case of the HTTP verb/method POST is create

The purpose of this method is to create a resource from the submitted payload.

#### query

#### payload

#### result

## GET
### The use case of the HTTP verb/method GET is read

The purpose of this method is to retrieve a resource according to resource

#### query

#### payload

#### result

## PATCH
### The use case of the HTTP verb/method PATCH is update

The purpose of this method is to update subsets( key, value pairs ) of a resource according to the submitted payload; utilizing both the submitted resource id and payload keys to overwrite only those keys mentioned in the payload when updating the datastore.

Pros: Will not touch values for keys not mentioned in payload

Pros and cons when comparing PATCH and PUT

#### query

#### payload

#### result

## PUT
### The use case of the HTTP verb/method PUT is overwrite

In essence this is exactly the same as running DELETE /:id and POST in sequence; however with a resource id
The purpose of this method is to overwrite a given resource according to the submitted payload

Pros: Can be used to overwrite an unwanted resource.
Cons: Used as update this will overwrite values for all keys not mentioned in payload.

Pros and cons when comparing PATCH and PUT

#### query

#### payload

#### result

## DELETE
### The use case of the HTTP verb/method DELETE is delete

The purpose of this method is to delete a resource according to its submitted key

#### query

#### payload

#### result
