![Alt text](<Simulator Screen Recording - iPhone 14 Pro Max - 2023-10-10 at 07.10.34.gif>)

# Notification list webview

> Features:

- Generate notification list view

- Authentication with Header

- Pull to refresh

- Infinite loading

Using view 3, typesciprt

## How to use
- 
- code example when integrate webview to flutter
```bash
var webView = WebView(
      initialUrl: '', // your webview url
      javascriptMode: JavascriptMode.unrestricted,
      onWebViewCreated: (WebViewController webViewController) {
        _controllerCompleter.future.then((value) => _controller = value);
        _controllerCompleter.complete(webViewController);
      },
      javascriptChannels: <JavascriptChannel>{
        JavascriptChannel(
          name: 'messageHandler',
          onMessageReceived: (JavascriptMessage message) {
            // do something
          },
        )
      },
    );
```

## Features will be updated in version 2

- PosmessageHandler to close webview

- Click to view detail notification

- update notification is read