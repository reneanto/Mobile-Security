
# Web Views

## What is Web View

* `WebView` Class is an Android's View Class extension which displays web pages as part of the activity layout, i.e it shows a web page when the activity is loaded.

```java
WebView myWebView = (WebView) findViewById(R.id.webview);
myWebView.loadUrl("http://www.example.com");
```

* So if the `WebView` class is used in an unsafe manner, the application is exposed to the usual web security vulnerabilities such as `xss, Open Redirect` .