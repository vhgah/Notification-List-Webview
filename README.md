![Alt text](<Simulator Screen Recording - iPhone 14 Pro Max - 2023-10-10 at 07.10.34.gif>)

# Notification list webview

> Features:

- Generate notification list view

- Authentication with Header

- Pull to refresh

- Infinite loading

Using view 3, typesciprt and tailwind.

## How to use
- create a index file html or php to load js and css file
```bash
https://vhgah.github.io/Notification-List-Webview/js/v1/index.js
```
```bash
https://vhgah.github.io/Notification-List-Webview/css/v1/index.css
```
index file example:
```bash
https://github.com/vhgah/Notification-List-Webview/blob/main/index.html
```
- make sure you has initInbox function to vue has access to your api get inboxes (listInboxUrl), authenToken (not required).
- and everything will work find.

## Example
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

## Api example
```bash
[
      {
            "title": "Alias vero magni doloremque minima est aperiam a.",
            "content": "Voluptates blanditiis ut ut sint eum soluta. Possimus dolor vel non alias vero optio inventore. Non ut voluptatem voluptatum et dignissimos. Harum .",
            "sent_at": "07-10-2023 16:25:20",
            "read_at": "08-10-2023 17:50:58",
            "image": "https://cdn-icons-png.flaticon.com/512/893/893257.png"
      },
]
```

## Features will be updated in version 2

- PosmessageHandler to close webview

- Click to view detail notification

- update notification is read

## Support

- If you have any issues or want to ask me: just create a new issue
