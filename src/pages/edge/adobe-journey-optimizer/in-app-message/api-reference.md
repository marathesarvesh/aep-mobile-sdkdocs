---
title: In-App Message - API Reference
description: This document lists the public APIs available in the Messaging extension for implementing in-app messaging.
keywords:
- Adobe Journey Optimizer
- API reference
- Messaging
- In-App Message
---

# In-App Messaging - API reference

This document lists the public APIs available in the Messaging extension for implementing in-app messaging.

## refreshInAppMessages

<InlineAlert variant="info" slots="text"/>

By default, the SDK will automatically fetch in-app message definitions from the remote at the time the Messaging extension is registered. This generally happens once per app lifecycle.

Some use cases may require the client to request an update from the remote more frequently. Calling the following API will force the Messaging extension to get an updated definition of messages from the remote:

<CodeBlock slots="heading, code" repeat="4" languages="Kotlin, Java, Swift, ObjC" />

#### Android

```kotlin
Messaging.refreshInAppMessages()
```

#### Android

```java
Messaging.refreshInAppMessages();
```

#### iOS

```swift
Messaging.refreshInAppMessages()
```

#### iOS

```objc
[AEPMobileMessaging refreshInAppMessages];
```
##updatePropositionForSurfaces

<InlineAlert variant="info" slots="text"/>
A dedicated surface for in-app (bundle Identifier) can be used as a default surface in this API. 

<CodeBlock slots="heading, code" repeat="4" languages="Kotlin, Java, Swift, ObjC" />

#### Android

```kotlin
let surface = Surface(name: "mobileapp://[bundleIdentifier]") //Dedicated surface for IAM
Messaging.updatePropositionsForSurfaces([surface])
```

#### Android

```java
let surface = Surface(name: "mobileapp://[bundleIdentifier]"); //Dedicated surface for IAM
Messaging.updatePropositionsForSurfaces([surface]);
```

#### iOS

```swift
let surface = Surface(name: "mobileapp://[bundleIdentifier]") //Dedicated surface for IAM
Messaging.updatePropositionsForSurfaces([surface])
```

#### iOS

```objc
AEPSurface* surface = [[AEPSurface alloc] initWithPath: @"mobileapp://[bundleIdentifier]"];
[AEPMobileMessaging updatePropositionsForSurfaces: @[surface]];
```
