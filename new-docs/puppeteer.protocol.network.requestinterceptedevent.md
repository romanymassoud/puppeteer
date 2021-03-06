<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [puppeteer](./puppeteer.md) &gt; [Protocol](./puppeteer.protocol.md) &gt; [Network](./puppeteer.protocol.network.md) &gt; [RequestInterceptedEvent](./puppeteer.protocol.network.requestinterceptedevent.md)

## Protocol.Network.RequestInterceptedEvent interface

Details of an intercepted HTTP request, which must be either allowed, blocked, modified or mocked. Deprecated, use Fetch.requestPaused instead.

<b>Signature:</b>

```typescript
export interface RequestInterceptedEvent 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [authChallenge](./puppeteer.protocol.network.requestinterceptedevent.authchallenge.md) | [AuthChallenge](./puppeteer.protocol.network.authchallenge.md) | Details of the Authorization Challenge encountered. If this is set then continueInterceptedRequest must contain an authChallengeResponse. |
|  [frameId](./puppeteer.protocol.network.requestinterceptedevent.frameid.md) | [Page.FrameId](./puppeteer.protocol.page.frameid.md) | The id of the frame that initiated the request. |
|  [interceptionId](./puppeteer.protocol.network.requestinterceptedevent.interceptionid.md) | [InterceptionId](./puppeteer.protocol.network.interceptionid.md) | Each request the page makes will have a unique id, however if any redirects are encountered while processing that fetch, they will be reported with the same id as the original fetch. Likewise if HTTP authentication is needed then the same fetch id will be used. |
|  [isDownload](./puppeteer.protocol.network.requestinterceptedevent.isdownload.md) | boolean | Set if the request is a navigation that will result in a download. Only present after response is received from the server (i.e. HeadersReceived stage). |
|  [isNavigationRequest](./puppeteer.protocol.network.requestinterceptedevent.isnavigationrequest.md) | boolean | Whether this is a navigation request, which can abort the navigation completely. |
|  [redirectUrl](./puppeteer.protocol.network.requestinterceptedevent.redirecturl.md) | string | Redirect location, only sent if a redirect was intercepted. |
|  [request](./puppeteer.protocol.network.requestinterceptedevent.request.md) | [Request](./puppeteer.protocol.network.request.md) |  |
|  [requestId](./puppeteer.protocol.network.requestinterceptedevent.requestid.md) | [RequestId](./puppeteer.protocol.network.requestid.md) | If the intercepted request had a corresponding requestWillBeSent event fired for it, then this requestId will be the same as the requestId present in the requestWillBeSent event. |
|  [resourceType](./puppeteer.protocol.network.requestinterceptedevent.resourcetype.md) | [ResourceType](./puppeteer.protocol.network.resourcetype.md) | How the requested resource will be used. |
|  [responseErrorReason](./puppeteer.protocol.network.requestinterceptedevent.responseerrorreason.md) | [ErrorReason](./puppeteer.protocol.network.errorreason.md) | Response error if intercepted at response stage or if redirect occurred while intercepting request. |
|  [responseHeaders](./puppeteer.protocol.network.requestinterceptedevent.responseheaders.md) | [Headers](./puppeteer.protocol.network.headers.md) | Response headers if intercepted at the response stage or if redirect occurred while intercepting request or auth retry occurred. |
|  [responseStatusCode](./puppeteer.protocol.network.requestinterceptedevent.responsestatuscode.md) | [integer](./puppeteer.protocol.integer.md) | Response code if intercepted at response stage or if redirect occurred while intercepting request or auth retry occurred. |

