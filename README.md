# ![LOGO](logo.png) Positioning **flow**ground Connector

## Description

A generated **flow**ground connector for the Positioning API (version 1.7.0).

Generated from: https://api.apis.guru/v2/specs/here.com/positioning/1.7.0/swagger.json<br/>
Generated at: 2019-05-07T17:42:16+03:00

## API Description

Positioning API for making location requests.

## Authorization

This API does not require authorization.

## Actions

### Locate

> Request WGS-84 compliant geocordinates for a location based on 2G/3G/4G cell and/or WLAN measurements.

#### Input Parameters
* `fallback` - _optional_ - Acceptable fallback options for cell and WLAN positioning. Values 'area' and 'any' apply to cell based positioning, and value 'singleWifi' applies to WLAN based positioning. They may both be combined in the same request.
By default cell based positioning returns cell tower level location estimates only. If you allow a WGS-84 compliant geocoordinate location estimate based on LAC, RNC, TAC, NID, or RZ areas, use the fallback=area setting. If you use the fallback=any setting, the service uses all available cell fallback methods and therefore the location estimate in the response may be at the MNC, SID, or MCC level.
For privacy reasons precise positioning based on a single WLAN AP is not possible. You can use the fallback=singleWifi setting to allow less accurate positioning based on a single WLAN AP. In that case the center location of the position estimate will be deviated and the reported accuracy radius will be larger.

    Possible values: any, area, singleWifi.
* `desired` - _optional_ - Comma-separated list of additional data fields that the service should include in the response if data is available. The query parameter supports the value 'altitude'.
    Possible values: altitude.
* `required` - _optional_ - Comma-separated list of additional data fields that the service should include in the response. If the data is not available, the response contains an error message. The query parameter supports the value 'altitude'.
    Possible values: altitude.
* `confidence` - _optional_ - Confidence level in percent for the accuracy/uncertainty in the location estimate response. If not specified, the default is 68 (this corresponds to a 68% probability that the true position is within the accuracy/uncertainty radius of the location estimate: the higher the number, the greater the confidence level).
* `app_id` - _required_ - A 20-byte Base64 URL-safe encoded string used for the authentication of the client application.
* `app_code` - _required_ - A 20-byte Base64 URL-safe encoded string used for the authentication of the client application.
* `Content-Encoding` - _optional_ - Indicates the data in the body is gzip encoded. Value must be 'gzip'.
    Possible values: gzip.
* `Content-Type` - _required_ - Indicates the media-type of the request body. Value must be 'application/json'.
    Possible values: application/json.

## License

**flow**ground :- Telekom iPaaS / here-com-positioning-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
