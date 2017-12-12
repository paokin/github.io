When you are building a sports book solution, you have a number of specific features and use cases in mind. Every individual feature needs to work with a specifically defined data set. For example, if you want to build a view for a sport event, you want to receive the name of this event, participants names, list of betting markets it contains, its current status, the league and sport it belongs to, etc. To fetch this type of data and subscribe to updates to it which will happen in the future, you want to use a query. The query is a part of a URL that is used to request specific data. We use The Open Data Protocol (OData) with some limitations and enhancements, as described below. The OData protocol uses JSON format, which is language independent.

Every entity type has a particular structure and defined fields. Site operators should use those specifics to obtain the desired data. First, you need to pick a collection. Depending on that, you have to query the respective endpoint. As already stated, our Sports data API exposes five endpoints:

* `/sports`
* `/leagues`
* `/events`
* `/markets`
* `/regions`

The overall pattern is as follows:

`[host]/api/[locale]/[apiname]/[apiversion]/[endpoint]/?query=[queryOption1]&[queryOption2]&...&[queryOptionN]`

* `[host]/api` – You will be provided with a base URL (which will have the [host]/api pattern) if you are authorised to use the Sports data API.
* `/[locale]` -- All of your queries should explicitly target a locale. If the locale you request is not supported, the response will fallback to the default English localisation.
* `/[apiname]` -- For the Sports data API this should equal `/sportsdata`.
* `/[apiversion]` -- The current and only version of the sports data is `/v1`.
* `/[endpoint]` -- As described in the the respective sections of the current document.
* `/?query=[queryOption1]&[queryOption2]&...&[queryOptionN]` -- As described in the the respective sections of the current document.

***

In this section:

* [Query Options](https://github.com/WeKnowSports/SportsDataAPI/wiki/Query-Options)
* [Query Option $filter Operators](https://github.com/WeKnowSports/SportsDataAPI/wiki/Query-Option-$filter-Operators)
* [Sports Data API Limitations](https://github.com/WeKnowSports/SportsDataAPI/wiki/Sports-Data-API-Limitations)