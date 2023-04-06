# NetSentry API Schema
**Url pattern**: `https://localhost:8080/<path>`

<br/>

**[POST]** `/webhooks/alert`
```js
{
    "severity": string,
    "data": {
        "name": string,          // Name of event
        "message": string,       // Additional message
        "port": integer,
        "protocol": string
    },
    "emittedTimestamp": integer  // Unix timestamp 
}
```
<br/>

**[POST]** `/webhooks/statsupdate`
```js
{
    "stats": {
        "totalPackets": {
            "value": integer
        },
        "bytesTransferred": {
            "value": integer
        }
    },
    "lastUpdated": integer,      // Unix timestamp when last update was sent
    "emittedTimestamp": integer  // Unix timestamp when event was emitted
}
```

