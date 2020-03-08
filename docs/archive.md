# Archive

Rest APIs which are related with accessing archive.

## Getting Archives
* GET <br> 
`archive/list?pageKey={}&pageSize={}`

* path param <br>
`pageKey` - key value for pagination  (optional) <br>
`pageSize` - pageSize from pageKey or latest (optional) <br> 

    If above fields are not provided, it will returns {pageSize (default 25)} archives from latest.
 
* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    archives|array|Required    
    archives.object.id|string|Required
    archives.object.thumbnailUrl|string|Required
    archives.object.title|string|Required
    nextPageKey|string|Optional
    
## Getting Images
* GET <br> 
`archive/{id}`

* path param <br>
  `id` - id of archived (required)

* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    title|string|Required
    thumbnailUrl|string|Required
    items|array|Required
    items.object.url|string|Required
    items.object.startTime|int|Required
    items.object.endTime|int|Required
    items.object.subtitle|string|Required