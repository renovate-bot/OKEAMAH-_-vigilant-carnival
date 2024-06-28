---
title: "PushSubscriptionOptions: applicationServerKey property"
short-title: applicationServerKey
slug: Web/API/PushSubscriptionOptions/applicationServerKey
page-type: web-api-instance-property
browser-compat: api.PushSubscriptionOptions.applicationServerKey
---

{{DefaultAPISidebar("Push API")}}{{SecureContext_Header}}

The **`applicationServerKey`** read-only property of the {{domxref("PushSubscriptionOptions")}} interface contains the public key used by the push server.

## Value

A public key your push server uses to send messages to client apps via a push server. This value is part of a signing key pair generated by your application server, and usable with elliptic curve digital signature (ECDSA), over the P-256 curve. If no `applicationServerKey` member is passed when initialized, it will be set to `null`.

## Examples

In the example below the value of `applicationServerKey` is printed to the console.

```js
navigator.serviceWorker.ready.then((reg) => {
  reg.pushManager.getSubscription().then((subscription) => {
    const options = subscription.options;
    console.log(options.applicationServerKey); // the public key
  });
});
```

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}