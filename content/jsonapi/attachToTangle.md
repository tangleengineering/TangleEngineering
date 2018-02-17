---
weight: 10
title: attachToTangle
---

## Attach To Tangle

This endpoint does the Proof of Work (PoW) required to attach a transaction to
the tangle. It's important to note that this doesn't actually do the attaching;
you must call `broadcastTransactions` to do that, but without doing the PoW
first your transaction will be deemed invalid by the network.


```shell
curl http://localhost:14265 \
  -X POST \
  -H 'Content-Type: application/json' \
  -H 'X-IOTA-API-Version: 1' \
  -d '{"command": "attachToTangle", "trunkTransaction": "JVMTDGDPDFYHMZPMWEKKANBQSLSDTIIHAYQUMZOKHXXXGJHJDQPOMDOMNRDKYCZRUFZROZDADTHZC9999", "branchTransaction": "P9KFSJVGSPLXAEBJSHWFZLGP9GGJTIO9YITDEHATDTGAFLPLBZ9FOFWWTKMAZXZHFGQHUOXLXUALY9999", "minWeightMagnitude": 18, "trytes": ["TRYTVALUEHERE"]}'

```

```go
package main

import (
    "github.com/iotaledger/giota"
    "fmt"
)

func main() {
    api := giota.NewAPI("http://localhost:14265",nil)

    // Still more to do here, ugh...

    request := giota.AttachToTangleRequest{
        TrunkTransaction: "JVMTDGDPDFYHMZPMWEKKANBQSLSDTIIHAYQUMZOKHXXXGJHJDQPOMDOMNRDKYCZRUFZROZDADTHZC9999",
        BranchTransaction: "P9KFSJVGSPLXAEBJSHWFZLGP9GGJTIO9YITDEHATDTGAFLPLBZ9FOFWWTKMAZXZHFGQHUOXLXUALY9999",
        MinWeightMagnitude: 14,
        Trytes: []giota.Transaction{
            transaction,
        },
    }
    response, err := api.AttachToTangle(&request)
    if err != nil {
        panic(err)
    }
    fmt.Printf("%#v\n",response)
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


