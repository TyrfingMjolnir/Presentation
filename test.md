# CRUOD - CRUD in full, Create, Read, Update, Overwrite, Delete

## POST
### The use case of the HTTP verb/method POST is create

The purpose of this method is to create a resource from the submitted payload.

## GET
### The use case of the HTTP verb/method GET is read

The purpose of this method is to retrieve a resource according to resource

## PATCH
### The use case of the HTTP verb/method PATCH is update

The purpose of this method is to update subsets( key, value pairs ) of a resource according to the submitted payload; utilizing both the submitted resource id and payload keys to overwrite only those keys mentioned in the payload when updating the datastore.

## PUT
### The use case of the HTTP verb/method PUT is overwrite

In essence this is exactly the same as POST; however with a resource id in its url.
The practical use is a delete of what is at the resource and replacing it with the payload, you can look at this either as a "secure"-delete or an expensive PATCH. 
The purpose of this method is to overwrite a given resource according to the submitted payload

## DELETE
### The use case of the HTTP verb/method DELETE is delete

The purpose of this method is to delete a resource according to its submitted key
