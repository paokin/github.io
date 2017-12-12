## Status Codes 

| HTTP Code | Description | Reason|
|----------|----------------|-----------|
|200|Successful HTTP request. The response depends on the requested data.|OK|
|400|The server cannot process the request. The reason might be incorrect syntax, invalid request, etc.|Bad Request|
|401|The authentication has failed.|Unauthorized|
|403|The request is valid, but the server refuses the action. The user might not have the necessary permissions for a resource or may need an account of some sort.|Forbidden|
|500| Unexpected condition occurred.|Server Error|

## Error Codes

| Error code | Message | Description |
|----------|------------------------------------------------------------------------------------------------------------------------|-----------|
| `code:1`  | The following fields aren't queryable: <name_of_fields>                                                                                        | The query cannot be applied to non-queryable fields. |
| `code:2`  | These fields cannot be combined: <name_of_field> and <name_of_field>                                                    | The query contains fields which cannot be queried simultaneously.|
|`code:7`|IncludeMarkets could query only Markets entity, not []|The query contains markets.|
| `code:10`  | Visit our wiki with supported entities http://... | The Sports Data API does not support requested entities. |
| `code:11` | The query cannot be processed by Odata parser. Exception message: ...                                                                                                      | If there are some mistakes in the syntax of query (e.g. incorrect name of fields, wrong query options or operators etc)|
| `code:12`  | The query shouldn't be empty! |The query is empty.|
| `code:13`    | | All other cases (e.g. "No gateways available") are displayed under this code.|