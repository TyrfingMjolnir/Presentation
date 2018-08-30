# CRUOD - CRUD in full, Create, Read, Update, Overwrite, Delete

## POST   
### The use case of the HTTP verb/method POST is create

The purpose of this method is to create a resource from the submitted payload.

#### query

```
http://localhost/user
```

#### payload

```
{
  "username":"User"
}
```

#### result ( in order to stay obedient to this format result is also shown as JSON )

```
{
  "username":"User"
}
```

## GET    
### The use case of the HTTP verb/method GET is read

The purpose of this method is to retrieve a resource according to resource

#### query

```
http://localhost/user/:id
```

#### payload

#### response 

```
{
  "username":"User"
}
```

## PATCH  
### The use case of the HTTP verb/method PATCH is update

The purpose of this method is to update subsets( key, value pairs ) of a resource according to the submitted payload; utilizing both the submitted resource id and payload keys to overwrite only those keys mentioned in the payload when updating the datastore.

Pros: Will not touch values for keys not mentioned in payload

^^ Pros and cons when comparing PATCH to PUT

#### query

```
http://localhost/user/:id
```

#### payload

```
{
  "phone":"1(555)123-4567",
  "mobile":"1(555)123-4568",
  "facsimile":"1(555)123-4569",
  "epost":"user@domain.tld",
  "fullname":"firstname lastname"
}
```

#### result

```
{
  "username":"User",
  "phone":"1(555)123-4567",
  "mobile":"1(555)123-4568",
  "facsimile":"1(555)123-4569",
  "epost":"user@domain.tld",
  "fullname":"firstname lastname"
}
```

## PUT    
### The use case of the HTTP verb/method PUT is overwrite

In essence this is exactly the same as running DELETE /:id and POST in sequence; however with a resource id
The purpose of this method is to overwrite a given resource according to the submitted payload

Pros: Can be used to overwrite an unwanted resource.

Cons: Used as update this will overwrite values for all keys not mentioned in payload.

^^ Pros and cons when comparing PATCH to PUT

#### query

```
http://localhost/user/:id
```

#### payload

```
{
  "fullname":"firstname lastname"
}
```

#### result

```
{
  "fullname":"firstname lastname"
}
```

## DELETE 
### The use case of the HTTP verb/method DELETE is delete

The purpose of this method is to delete a resource according to its submitted key

#### query

```
http://localhost/user/:id
```

#### payload

#### result
[]
