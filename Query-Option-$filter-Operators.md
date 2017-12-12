The `$filter` system query option allows clients to filter a collection of resources that are addressed by a request URL. The expression specified with `$filter` (or with `$includeMarkets` in the special case of the `/events` endpoint) is evaluated for each resource in the collection, and only items where the expression evaluates to true are included in the response. The objects can be filtered based on any of the queriable attributes.

|Operator|Description| Example| Value Type|
|--------|-----------|--------|-----------|
|ne|Not equal|js $filter=sportId ne '1'|boolean, integer, string, datetime|
|lt|Less than|-|integer, datetime|
|le|Less than or equal|-|integer, datetime|
|gt|Greater than|-|integer, datetime|
|ge|Greater than or equal|-|integer, datetime|
|and|Logical and|js $filter=SportId eq '1' and LeagueId eq '13761'|boolean, integer, string, datetime|
|or|Logical or|js $filter=SportId eq '1' or SportId eq '5'|boolean, integer, string, datetime|

OData allows querying by a nested property. This means that you can filter a list of entities based on a property of an object, which is itself as a value for a property of the main entity. Example: `Markets?$filter=MarketType/id eq '1_39'`