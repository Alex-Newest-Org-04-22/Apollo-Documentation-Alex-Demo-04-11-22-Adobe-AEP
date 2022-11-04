# Order Placed

### 

## Javascript Code
```js
window.appEventData = window.appEventData || [];
appEventData.push({
  "event": "Order Placed",
    "cart": {
        "cartID": "<cartID>"
    },
    "transaction": {
        "item": [
            {
                "altPersonPickUp": <altPersonPickUp>,
                "fulfillment": {
                    "method": "<method>",
                    "source": "<source>",
                    "storeID": "<storeID>"
                },
                "pickUpTextNotifications": <pickUpTextNotifications>,
                "price": {
                    "basePrice": "<basePrice>",
                    "markdownPrice": "<markdownPrice>",
                    "priceTier": "<priceTier>",
                    "priceType": "<priceType>",
                    "sellingPrice": "<sellingPrice>"
                },
                "productInfo": {
                    "brand": "<brand>",
                    "businessUnit": "<businessUnit>",
                    "color": "<color>",
                    "isGiftWrapped": <isGiftWrapped>,
                    "isSample": "<isSample>",
                    "name": "<name>",
                    "productID": "<productID>",
                    "productLine": "<productLine>",
                    "sku": "<sku>",
                    "thirdyPartyVendorID": "<thirdyPartyVendorID>",
                    "trademarkedTechnology": "<trademarkedTechnology>",
                    "webExclusive": <webExclusive>
                },
                "quantity": <quantity>,
                "shippingAddress": {
                    "country": "<country>",
                    "postalCode": "<postalCode>",
                    "stateProvince": "<stateProvince>"
                },
                "shippingCost": "<shippingCost>",
                "shippingMethod": "<shippingMethod>",
                "shippingVoucherCode": "<shippingVoucherCode>",
                "shippingVoucherDiscount": "<shippingVoucherDiscount>",
                "tax": "<tax>",
                "voucherDiscount": {
                    "orderLevelDiscountAmount": "<orderLevelDiscountAmount>",
                    "orderLevelDiscountCode": "<orderLevelDiscountCode>",
                    "productLevelDiscountAmount": "<productLevelDiscountAmount>",
                    "productLevelDiscountCode": "<productLevelDiscountCode>"
                }
            }
        ],
        "payment": [
            {
                "loyaltyPointsAmount": <loyaltyPointsAmount>,
                "paymentAmount": "<paymentAmount>",
                "paymentGateway": "<paymentGateway>",
                "paymentID": "<paymentID>",
                "paymentMethod": "<paymentMethod>",
                "paymentSequence": <paymentSequence>
            }
        ],
        "productIDList": "<productIDList>",
        "profile": {
            "address": {
                "country": "<country>",
                "postalCode": "<postalCode>",
                "stateProvince": "<stateProvince>"
            }
        },
        "purchaseID": "<purchaseID>",
        "skuList": "<skuList>",
        "total": {
            "currency": "<currency>",
            "numPayments": <numPayments>,
            "revenue": "<revenue>"
        },
        "transactionID": "<transactionID>"
    }
});
```

## Variable Definitions

|Path|Type|Description|Example|Pattern|Min Length|Max Length|Minimum|Maximum|Multiple Of|
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|cart.cartID|string|Back-end identifier for a shopping cart|12345, 435678, 34567, XCV456, XCV876|||||||
|transaction.item[n].altPersonPickUp|integer|When a user has put in the information of an alternate pick up person during the checkout process.||||||||
|transaction.item[n].fulfillment.method|string|Describes the method of fulfillment|Shipped, Emailed, Pick Up In Store, Will Call|||||||
|transaction.item[n].fulfillment.source|string|Describes the entity responsible for fulfillment. Uasge is flexible.|Vendor:xyz, Store:43567, Email:system3, Warehouse:7865|||||||
|transaction.item[n].fulfillment.storeID|string|A unique identifier for the store that the order was placed with.|stew's boot shop, kat's cat toys, 12345|||||||
|transaction.item[n].pickUpTextNotifications|integer|The count of times a user has selected to receive text notifications during the checkout process.||||||||
|transaction.item[n].price.basePrice|string|String representation of MSRP of a product. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].price.markdownPrice|string|String representation of the price offered. Often called 'hard mark' price. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].price.priceTier|string|Describes the general pricing tier of a product. \(Good, Better, Best\)|Good, Better, Best, Bronze, Silver, Gold|||||||
|transaction.item[n].price.priceType|string|Describes the type of price offered using commonly used terms. |1st mark, 2nd mark, 3rd mark, clearance, sale, doorbuster|||||||
|transaction.item[n].price.sellingPrice|string|String representation of the price paid after coupons or discounts. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].productInfo.brand|string|Describes the brand of a product or offering.|Ford, Chevrolet, Dodge, Levis, Columbia, Patagonia|||||||
|transaction.item[n].productInfo.businessUnit|string|The business unit associated with each product.|Apparel, Shoes, Home|||||||
|transaction.item[n].productInfo.color|string|Describes the colorway of a product or product variant|Antique Oak, Granite, Black Marble, Knotty Pine|||||||
|transaction.item[n].productInfo.isGiftWrapped|boolean|At order confirmaton, set a to true for every product that is gift wrapped.||||||||
|transaction.item[n].productInfo.isSample|string|True\/False flag to indicate if the product is a sample.|true, false|||||||
|transaction.item[n].productInfo.name|string|Name of the product or offering.  Should be unique and 1:1 with productID|Oceana, Corsica, Flame Tech, Air Jordan 88|||||||
|transaction.item[n].productInfo.productID|string|Unique Identifier of a product or offering.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level above SKU for products with SKU variants. |155, 65588, 987764448|||||||
|transaction.item[n].productInfo.productLine|string|Describes the product Line of a product. |Laminate Wood, Vinyl, Hardwood, Stone, Ceramic|||||||
|transaction.item[n].productInfo.sku|string|Stock Keeping Unit \(SKU\) Unique Identifier of specific item \(typically\) held in inventory.  Must match the format of back-end systems if used as a key for import of product meta data. Most often, one level below productID for products with SKU variants. |34567890, 4567890, 00155-large-cornflower|||||||
|transaction.item[n].productInfo.thirdyPartyVendorID|string|Captures the vendor id of the third party vendor associated with product conversion.||||||||
|transaction.item[n].productInfo.trademarkedTechnology|string|Describes trademarks and\/or technical branding used to describe the product|Stainmaster, GoreTex, WeatherShield|||||||
|transaction.item[n].productInfo.webExclusive|boolean|Captures whether or not the product is sold on website\/app only.||||||||
|transaction.item[n].quantity|integer|Integer number of products being acted upon \(added to a cart, removed from wishlist, purchased, reserved\)|1, 2, 3, 4, 5||||1|||
|transaction.item[n].shippingAddress.country|string|Indicates the country of the address of the shipment. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|transaction.item[n].shippingAddress.postalCode|string|The mailing zip or postal code associated with the address of the shipment. |53533, 30381, M1R 0E9, M3C 0C1|||||||
|transaction.item[n].shippingAddress.stateProvince|string|The mailing state or province associated with address of the shipment. |WI, GA, NB, ON|||||||
|transaction.item[n].shippingCost|string|The shipping costs for all items within the shippingGroup of the transaction.|15.05, 2, 0.22, 2.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].shippingMethod|string|Describes the method or carrier and method of shipment. Should be common terminology within your business. |Regular, Overnight, Overnight AM, Overnight AM Sat, UPS Ground, UPS Air|||||||
|transaction.item[n].shippingVoucherCode|string|Discount code applied against shipping costs for a shipping Group|FREESHIPAPRIL, FREESHIP100|||||||
|transaction.item[n].shippingVoucherDiscount|string|String representation of an discount applied against shipping costs for a shipping group. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].tax|string|String representation of the tax collected at a shipment level for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5.05, 20, 10.22, 9.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].voucherDiscount.orderLevelDiscountAmount|string|String representation of an order level discount applied to an item in a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].voucherDiscount.orderLevelDiscountCode|string|Order Level Discount code applied at the item level of a transaction. |FRIENDSANDFAMILY20, EASTER10|||||||
|transaction.item[n].voucherDiscount.productLevelDiscountAmount|string|String representation of product level discount for a transaction. Positive. Up to two decimal places for cents. No currency symbol.|5, 20, 10.22, 19.2|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.item[n].voucherDiscount.productLevelDiscountCode|string|Discount code applied for a specific item \(or items\) of a transaction. |5OFFSHOES, AKRONCANDLES2019|||||||
|transaction.payment[n].loyaltyPointsAmount|integer|Number of loyalty points |100, 101, 1000||||0|||
|transaction.payment[n].paymentAmount|string|String representation of the payment amount. Positive. Up to two decimal places for cents. No currency symbol.|200, 29.99, 50, 0|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.payment[n].paymentGateway|string|Captures the digital payment gateway was used to complete transactions for orders?|PayPal, Stripe|||||||
|transaction.payment[n].paymentID|string|Unique identifier of a payment.  Typically an integration key from a back-end system.|ZPH-87698-098|||||||
|transaction.payment[n].paymentMethod|string|Describes the method of payment for a transaction. |Credit Card, PayPal, Mastercard, Visa, Amex, Discover|||||||
|transaction.payment[n].paymentSequence|integer|Integer indicator of the sequence in which payments were applied within a transaction.  Starting with 1.|1, 2, 3, 4, 5||||1|||
|transaction.productIDList|string|A delimited list of product IDs in the transaction.|1234\|7878\|9039, abc12\|deh213, abc12|||||||
|transaction.profile.address.country|string|Indicates the country of the billing address. ISO 3166 \(alpha-2\) Uppercase.|US, CA, FR, UK|^[A-Z]{2}$||||||
|transaction.profile.address.postalCode|string|The mailing zip or postal code associated with the billing address. |53533, 30381, M1R 0E9, M3C 0C1|||||||
|transaction.profile.address.stateProvince|string|The mailing state or province associated with billing address. |WI, GA, NB, ON|||||||
|transaction.purchaseID|string|Unique identifier of the purchase. Max Length 20. Used as Unique ID of the purchase or deduplication.|ABC-132456789, DEF-132456789, 0987654567|^[a-zA-Z0-9]{6,20}$|6|20||||
|transaction.skuList|string| A delimited list of skus in the transaction.|sku123\|sku465, 67890\|87576\|74674, 87654|||||||
|transaction.total.currency|string|Currency of the transaction. ISO 4217 \(3 character alpha\), uppercase |USD, CAD, GBP, CHF|^[A-Z]{3}$|3|3||||
|transaction.total.numPayments|integer|Collects the number of payment methods used for an order at order confirmaton||||||||
|transaction.total.revenue|string|The total revenue for a transaction. Does not include tax or shipping. |125.05, 432.21, 90.22, 12.05|^[0-9]*(\.[0-9]{1,2})?$||||||
|transaction.transactionID|string|Unique identifier of the transaction. Max Length 100. Used as a key for upload of post transaction data. |123e4567-e89b-12d3-a456-426614174000|^[a-zA-Z0-9]{6,100}$|6|100||||




