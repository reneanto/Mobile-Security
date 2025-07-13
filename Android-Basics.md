


## Intents


*Through Intents, the Android apps communicate between their components and other apps.*

They carry data between apps/components just like GET/POST requests in HTTP communications.

Intents are generally used to/as :

* Start an activity.
* Broadcasts to inform the system and app changes.
* Start/stop or communicate with background services.
* access data via ContentProviders.
* callbacks as event handlers.

Intents if not declared securely can be vulnerable.

### Intent-Filters

*They define how an activity,service or a Broadcast receiver can interact with different types of intents.*

They consist of categories, actions and data filters, also can include additional metadata

A component is considered public and can interact with other apps if it is "exported" with the value of "true" or if an Intent filter is declared for it in the manifest.

The "Permission" attribute is set to enforce that the apps with designated permissions only can  access the component.



### Implicit Intents

Intents that are programatically created using an Intent Constructor.

```java
Intent email = new Intent(Intent.ACTION_SEND, Uri.parse("mailto:"));
```

Inside `androidmanifest.xml` 


```xml
<activity android:name="ShareActivity">
    <intent-filter>
       <action android:name="android.intent.action.SEND" />
       <category android:name="android.intent.category.DEFAULT" />
    </intent-filter>
</activity>
```

An intent-filter need to match the action,data and category to receive a message.


### Explicit Intent

This intent specifies the class name it's targeting

``` java
Intent downloadIntent = new (this, DownloadService.class):
```


In the other app

``` java
Intent intent = new Intent();
intent.setClassName("com.other.app", "com.other.app.ServiceName");
context.startService(intent);
```