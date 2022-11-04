# Product Added to Cart

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Product Added to Cart",
    "cart": {
        "additionContext": "<additionContext>",
        "cartID": "<cartID>",
        "cartModifications": <cartModifications>
    },
    "eventDetails": {
        "multiAdditionDetail": "<multiAdditionDetail>",
        "multiAdditions": <multiAdditions>
    },
    "product": [
        {
            "fulfillment": {
                "isBopusOnly": <isBopusOnly>,
                "method": "<method>"
            },
            "price": {
                "priceTier": "<priceTier>",
                "priceType": "<priceType>",
                "sellingPrice": "<sellingPrice>"
            },
            "productInfo": {
                "brand": "<brand>",
                "businessUnit": "<businessUnit>",
                "color": "<color>",
                "isOffer": <isOffer>,
                "isOutOfStock": <isOutOfStock>,
                "isSample": "<isSample>",
                "name": "<name>",
                "productID": "<productID>",
                "productLine": "<productLine>",
                "sku": "<sku>",
                "thirdyPartyVendorID": "<thirdyPartyVendorID>",
                "trademarkedTechnology": "<trademarkedTechnology>",
                "webExclusive": <webExclusive>
            },
            "quantity": <quantity>
        }
    ]
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cart.additionContext|string|Conveys the context of a cart addition. |PLP, PDP, Wishlist, Registry|||||||
|cart.cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|cart.cartModifications|integer|Count of times the change in product quantity was the result of a cart modification.||||||||
|eventDetails.multiAdditionDetail|string|Provides details of multiple product additions to carts, wishlists, registries, etc.|all items, 3 of 5, 2 of 4|||||||
|eventDetails.multiAdditions|boolean|Flag indicating whether multilple products where added to carts, wishlists, registries, etc.|true, false|||||||
|product[n].fulfillment.isBopusOnly|integer|Count of times the user engaged with a product whose only available shipping method was Buy Online Pick Up In Store \(i.e., BOPUS\).||||||||
|product[n].fulfillment.method|string|Captures the shipping fullfilment method associated with a product.||||||||
|product[n].price.priceTier|string|Describes the general pricing tier of a product. \(Good, Better, Best\)|Good, Better, Best, Bronze, Silver, Gold|||||||
|product[n].price.priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|product[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|product[n].productInfo.brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|product[n].productInfo.businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|product[n].productInfo.color|string|Describes the colorway of a product or product variant|Antique Oak, Granite, Black Marble, Knotty Pine|||||||
|product[n].productInfo.isOffer|integer|Count of times an offered product \(e.g., Gift with Purchase, Purchase with Purchase\) is added to the cart.||||||||
|product[n].productInfo.isOutOfStock|boolean|Boolean flag indicating that an inventoried product is out of stock. |TRUE, FALSE|||||||
|product[n].productInfo.isSample|string|True\/False flag to indicate if the product is a sample.|true, false|||||||
|product[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|product[n].productInfo.productLine|string|Describes the product Line of a product. |Laminate Wood, Vinyl, Hardwood, Stone, Ceramic|||||||
|product[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|product[n].productInfo.thirdyPartyVendorID|string|Captures the vendor id of the third party vendor associated with product conversion.||||||||
|product[n].productInfo.trademarkedTechnology|string|Describes trademarks and\/or technical branding used to describe the product|Stainmaster, GoreTex, WeatherShield|||||||
|product[n].productInfo.webExclusive|boolean|Captures whether or not the product is sold on website\/app only.||||||||
|product[n].quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||




