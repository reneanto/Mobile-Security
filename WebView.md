# Web Views

## What is Web View

* `WebView` Class is an Android's View Class extension which displays web pages as part of the activity layout, i.e it shows a web page when the activity is loaded.

```java
WebView myWebView = (WebView) findViewById(R.id.webview);
myWebView.loadUrl("http://www.example.com");
```

* So if the `WebView` class is used in an unsafe manner, the application is exposed to the usual web security vulnerabilities such as `xss, Open Redirect` .

### References

* [Android-Security-Checklist-Webview](https://blog.oversecured.com/Android-security-checklist-webview/)
* [Webview-Unsafe-File-Inclusion](https://developer.android.com/privacy-and-security/risks/webview-unsafe-file-inclusion)
* [Unsafe-URI-Loading](https://developer.android.com/privacy-and-security/risks/unsafe-uri-loading)
* [Insecure-WebView-Native-Bridges](https://developer.android.com/privacy-and-security/risks/insecure-webview-native-bridges)
* [MASTG-0x05h-Testing Platform-Interaction](https://mas.owasp.org/MASTG/0x05h-Testing-Platform-Interaction/#webviews)