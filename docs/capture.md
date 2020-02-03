# Capture

Rest APIs which are related with Capture.

## Capturing Images
* POST <br> 
`capture/`

* body param

    Parameter | Type | Required / Optional | 
    :-----------: |:-------------:|:-------------:| 
    |url|string|required|
    |language|string|optional (default = eng)|
    |numberToCapture|int|optional|
    |startTimeStamp|int|optional|
    |endTimeStamp|int|optional|

* response

    Name | Type |Require/Optional| 
    :-----------:|:-------------:|:-------------:|
    id|string|Required
    title|string|Required   
    captureItems|array|Required
    captureItems.object.url|string|Required
    captureItems.object.startTime|int|Required
    captureItems.object.endTime|int|Required
    captureItems.object.subtitle|string|Required