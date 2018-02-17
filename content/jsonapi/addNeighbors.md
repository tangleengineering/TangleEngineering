---
weight: 10
title: addNeighbors
---

## Add Neighbors
This endpoint allows you to add new neighbors to IRI. It returns the total
number of neighbors that were successfully added.  


```shell
curl http://localhost:14265 \
  -X POST \
  -H 'Content-Type: application/json' \
  -H 'X-IOTA-API-Version: 1' \
  -d '{"command": "addNeighbors", "uris": ["udp://8.8.8.8:14265", "udp://8.8.8.5:14265"]}'

```

```go
package main

import (
    "github.com/iotaledger/giota"
    "fmt"
)

func main() {
    api := giota.NewAPI("http://localhost:14265",nil)
    neighbors, err := api.AddNeighbors("udp://8.8.8.8:14265", "udp://8.8.8.5:14265")
    if err != nil {
        panic(err)
    }
    fmt.Printf("%#v\n",neighbors)
}
```

```javascript
// Someone please contribute
```

```python
# Someone please contribute
```

```java
// Someone please contribute
```

> Make sure to replace `http://localhost:14265` with the hostname and port of
> an IRI node if you are not running one yourself.


### Response

Considering changing the `value` column below to be a description of the
returned value instead of an example. 

Field Name | Value
-----------|-------
addedNeighbors|2
