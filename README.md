# Auction

Auction extension which shows all auction properties of lots and tender

## Overview
Auction can be represented using an array of auction blocks in the 
auctions field of the tender and a web address for participation in auction in
bid of an OCDS release.

The web address for view auction can be represented as string using the 
auctions/url field.

The period when auction is conducted should be provided using the 
auctions/period field. The value of it must be Period object.

The minimal step for this auction should be represented as
value of auctions/minimalStep field. The value of it must be 
Value object.

A web address for participation in auction can be provided as string using 
the participationUrl field in bid.

## Examples
The example below shows a auction in tender and a auction link in bid.
```
{
  "tender": {
    "auctions": [
      {
        "url": "https://auction.openprocurement.org/tenders/001b2c1c3c4f42b4a17b2c565fb86a2f_a361be2dfd9df53ab70764e4caab6a47",
        "period": {
          "startDate": "2018-01-09T14:49:48+02:00",
          "endDate": "2018-01-09T15:16:49.199756+02:00"
        },
        "minimalStep": {
          "currency": "UAH",
          "amount": 1208090.2,
          "valueAddedTaxIncluded": true
        }
      }
    ]
  },
  "bids": [
    {
      "participationUrl": "https://auction.openprocurement.org/tenders/001b2c1c3c4f42b4a17b2c565fb86a2f_a361be2dfd9df53ab70764e4caab6a47/login?bidder_id=e18852575cbe46c497d7925c73bebc2d&hash=395ff2e48e5d8b00c2d22dd272bcd3ebf961a157"
    }
  ]
}
```