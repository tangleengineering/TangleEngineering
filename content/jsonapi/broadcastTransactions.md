---
weight: 10
title: broadcastTransactions 
---

## Broadcast Transactions

This endpoint returns information about the IRI node you have connected to,
including software name and version as well as what the latest milestones it has
seen are.


```shell
curl http://localhost:14265 \
  -X POST \
  -H 'Content-Type: application/json' \
  -H 'X-IOTA-API-Version: 1' \
  -d '{"command": "getNodeInfo"}'

```

```go
package main

import (
    "github.com/iotaledger/giota"
    "fmt"
)

func main() {
    api := giota.NewAPI("http://localhost:14265",nil)
    nodeInfo, err := api.GetNodeInfo()
    if err != nil {
        panic(err)
    }
    fmt.Printf("%#v\n",nodeInfo)
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
appName|IRI
appVersion|1.4.2.1
jreAvailableProcessors|4
jreFreeMemory|466437760
jreVersion|1.8.0_162
jreMaxMemory|7874281472
jreTotalMemory|3077570560
latestMilestone|9CVOPWUEEA9OGDP9BUJOUWYLFWYQORDYZEFLPVH9RDOBHZYTVHBWIYHYIOYGLVKKCMHKE9HTXGIEA9999
latestMilestoneIndex|350201
latestSolidSubtangleMilestone|9CVOPWUEEA9OGDP9BUJOUWYLFWYQORDYZEFLPVH9RDOBHZYTVHBWIYHYIOYGLVKKCMHKE9HTXGIEA9999
latestSolidSubtangleMilestoneIndex|350201
neighbors|11
packetsQueueSize|0
time|1518634288522
tips|5454,
transactionsToRequest|50
duration|0


