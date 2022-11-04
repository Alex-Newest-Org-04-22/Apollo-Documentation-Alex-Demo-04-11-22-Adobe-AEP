# Content Listing Displayed

### This event is part of the page load sequence, including virtual page loads in the case of single page apps, and must be pushed between the `Page Load Started` and `Page Load Completed` events.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Content Listing Displayed",
    "listingDisplayed": {
        "displayCount": <displayCount>,
        "filterListLength": <filterListLength>,
        "listing": [
            {
                "content": {
                    "contentAuthor": "<contentAuthor>",
                    "contentDate": "<contentDate>",
                    "contentID": "<contentID>",
                    "contentTitle": "<contentTitle>"
                },
                "isDisplayed": <isDisplayed>
            }
        ],
        "listingContext": "<listingContext>",
        "listingDriver": "<listingDriver>",
        "listingType": "<listingType>",
        "resultsCount": <resultsCount>,
        "sortDefault": <sortDefault>,
        "sortOrder": "<sortOrder>"
    },
    "listingRefined": {
        "filterList": "<filterList>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|listingDisplayed.displayCount|integer|The total number of items displayed out of all returned items. \(Integer\)|10, 20, 30, 40||||0|||
|listingDisplayed.filterListLength|integer|The number of filterValue pairs in the filterList|0, 20, 12||||0|||
|listingDisplayed.listingContext|string|Describes the context of a listing display \(sort changed, filter added, filter removed\)|Filter Added, Filter Removed, Sort Change, Pagination|||||||
|listingDisplayed.listingDriver|string|Describes the action that caused the listing to be displayed|Onsite Search, Curated Assortment, Navigation|||||||
|listingDisplayed.listingType|string|The type of results being listed|text, product, location, event, room, product location|||||||
|listingDisplayed.listing[n].content.contentAuthor|string|Unique identifer of the content author.|Betsy Ross, Ben Franklin, Howard Hughes, Tipper Gore|||||||
|listingDisplayed.listing[n].content.contentDate|string|Date of the content's publication. ISO 8601 form \(YYYY-MM-DD\). Jan 1, 2019 is 2019-01-01|2001-12-22, 2011-01-01|^([0-9]{4})-(1[0-2]|0[1-9])-(3[01]|0[1-9]|[12][0-9])$||||||
|listingDisplayed.listing[n].content.contentID|string|Unique identifer of the content.||||||||
|listingDisplayed.listing[n].content.contentTitle|string|Title of a piece of content. |50 ways to use jello, Another look at pandas, Year end giving|||||||
|listingDisplayed.listing[n].isDisplayed|boolean|Helper node used by AA Product String Builder to set product scoped events|true|||||||
|listingDisplayed.resultsCount|integer|The total number of items returned that matched the search criteria. \(Integer\)|1, 21, 111, 166||||0|||
|listingDisplayed.sortDefault|integer|The default sort value on listings|A to Z, Low to High, Newest to Oldest||||0|||
|listingDisplayed.sortOrder|string|Indicates the sort order.|high-low, low-high, nearest-farthest, a-z, newest-oldest|||||||
|listingRefined.filterList|string|A twice delimited string of filterType and filterValue pairs.  Use \~ between type and value.  Use \| between pairs|sort\~price ascending\|color\~green\|size\~medium|||||||




