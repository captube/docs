# Archive

Rest APIs which are related with accessing archive.

## Getting Archives
* GET <br> 
`archive/list?pageFrom={}&pageTo={}`

* path param <br>
`pageFrom` - start number of page (optional) <br> 
`pageFrom` - end number of page (optional)
 
* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    id|string|Required
    title|string|Required
    
## Getting Images
* GET <br> 
`archive/{id}`

* path param <br>
  `id` - id of archived (required)

* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    title|string|Required
    items|Array|Required
    items.object.url|string|Required
    items.object.startTime|int|Required
    items.object.endTime|int|Required
    items.object.subtitle|string|Required