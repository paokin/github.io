Sports Data API is subject to some usage limits.

All calls to the Sports Data API will return a maximum of 500 items in the response. This means that every query is implicitly appended with `&$top=500` option. If more than 500 items are requested explicitly, an error message will appear.

The query can contain a time range to reduce the size of the response further. Respectively, filtering by datetime attributes is not possible. Specifically, the startEventDate attribute for events and startDate attribute for markets are non-queriable. You should use these static time range modifiers in your query instead.

Queries to the events endpoint can contain an IncludeMarkets filter, which is applied to the market entities related to the respective events. If the query doesn't contain IncludeMarkets filter, only the markets tagged as Default will be available in the response. Note that the markets which are returned this way do not count against the limitation of maximum 500 items in the response.