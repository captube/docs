# Archive

Rest APIs which are related with accessing archive.

## Getting Archives
* GET <br> 
`archive/list?pageFrom={}&pageTo={}`

* path param <br>
`pageFrom` - start number of page (optional) <br> 
`pageTo` - end number of page (optional) <br>

    If above field is not provided, it will returns all of the archives
 
* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    archives|array|Required    
    archives.object.id|string|Required
    archives.object.title|string|Required
    
## Getting Images
* GET <br> 
`archive/{id}`

* path param <br>
  `id` - id of archived (required)

* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    title|string|Required
    items|array|Required
    items.object.url|string|Required
    items.object.startTime|int|Required
    items.object.endTime|int|Required
    items.object.subtitle|string|Required