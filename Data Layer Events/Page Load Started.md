# Page Load Started

### Page Load Started is part of the page load sequence, including virtual page loads in the case of single page apps, and must be the first event pushed in the page load event sequence.

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Page Load Started",
    "page": {
        "breadcrumbs": "<breadcrumbs>",
        "dayOfWeek": "<dayOfWeek>",
        "detailedPageName": "<detailedPageName>",
        "flowStep": "<flowStep>",
        "internalBusinessOwner": "<internalBusinessOwner>",
        "isIncognitoMode": <isIncognitoMode>,
        "pageCategory": "<pageCategory>",
        "pageExperience": "<pageExperience>",
        "pageName": "<pageName>",
        "pageTitle": "<pageTitle>",
        "pageType": "<pageType>",
        "platform": "<platform>",
        "releaseVersion": "<releaseVersion>",
        "siteCountry": "<siteCountry>",
        "siteCurrency": "<siteCurrency>",
        "siteExperience": "<siteExperience>",
        "siteLanguage": "<siteLanguage>",
        "siteName": "<siteName>",
        "siteType": "<siteType>",
        "subsection": "<subsection>",
        "subsection2": "<subsection2>",
        "subsection3": "<subsection3>",
        "weekdayOrWeekend": "<weekdayOrWeekend>"
    },
    "page_data": {
        "hour": "<hour>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|page.breadcrumbs|string|A delimited list of hierarchical sections that describe the current page's location within the navigation of the site.|Home&gt;Women&gt;Tops&gt;Sweaters, Mens - Tops - Sweaters - Supmina, Wool, Rayon, Checkout &gt; Order Thank You|||||||
|page.dayOfWeek|string|The day of the week the activity occured.||||||||
|page.detailedPageName|string|Describes the page in more detail than the pageName attribute|product - XYZ123 - super cotton neck scarf, Mens - Tops - Sweaters - Supmina, Wool, Rayon, Order Confirmation - 098fghjkl|||||||
|page.flowStep|string|Describes the step withing a multi-step process or flow.|Booking 2.a, Booking 2.b, Booking 3, Booking 4|||||||
|page.internalBusinessOwner|string|Describes the internal team who manages this particular page of the website.|XX product management, marketing, vendor name|||||||
|page.isIncognitoMode|integer|Set on all pages when user is in "incognito mode" in their browser.||||||||
|page.pageCategory|string|General category or Site Section of the page. Top level of page hierarchy.|Home, About Us, Shop, Account, Blog, Investors|||||||
|page.pageExperience|string|When a feature ramp up is taking place, capture a code to identify users receiving that feature's experience.||||||||
|page.pageName|string|Describes the page and its content specifically. |product - XYZ123, Mens - Tops - Sweaters, Order Confirmation|||||||
|page.pageTitle|string|HTML title tag for the page||||||||
|page.pageType|string|Describes what purpose the page serves. Often aligns with the CMS template.|Home, Event Detail, Property Detail, Product Listing, Blog Post, Shopping Cart|||||||
|page.platform|string|The technology platform version of the site that the user is experiencing.||||||||
|page.releaseVersion|string|Set to the information about the technology release that is most current on the page.||||||||
|page.siteCountry|string|Indicates the primary country served by the site. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|page.siteCurrency|string|Currency in which prices are displayed.  ISO 4217 \(3 character alpha\), uppercase|USD, CAD, EUR, GBP, CHF|^[A-Z]{3}$||||||
|page.siteExperience|string|Describes the version of the site that is being shown|Responsive, Mobile, Desktop|||||||
|page.siteLanguage|string|Language in which the site is presented ISO 639-1 code. |en-us, en-gb, ch-cn, fr-ca, fr-fr, da|^[a-z]{2}([-]{1}[a-z]{2}){0,1}$||||||
|page.siteName|string|Common language used within the business to refer to the website. May be specific County Sites.|Prospecting-EU, Prospecting-US, Member Portal, Shop-CA, Shop-US, Shop-EU|||||||
|page.siteType|string|Common language description of the site type of purpose. May be used to group siteName.|Prospecting, Shop, Members, Brand|||||||
|page.subsection|string|First sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids, Shop &gt; Mens, Shop &gt; Womens|||||||
|page.subsection2|string|Second sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids &gt; Tops, Shop &gt; Mens &gt; Shoes|||||||
|page.subsection3|string|Third sub-level of hierarchy under pageCategory or Site Section. |Shop &gt; Kids &gt; Tops &gt; Tees, Shop &gt; Mens &gt; Shoes &gt; Oxfords|||||||
|page.weekdayOrWeekend|string|Whether it was a week day or weekend when activity is occurred.||||||||
|page_data.hour|string|The time of activity at the top of the hour.||||||||




