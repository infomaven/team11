# team11
Application for *Hack like a Girl* at Nike WHQ, Feb 2015




<a target="_blank" href="https://chrome.google.com/webstore/detail/nmfpplkdkcbhediajmbhljkafnlahcda">![Try it now in CWS](https://raw.github.com/GoogleChrome/chrome-app-samples/master/tryitnowbutton.png "Click here to install this sample from the Chrome Web Store")</a>


# REACH

REACH is a web application designed as a portal to help women who want to improve their tech skills find mentors and other women with similar interests. Members can create online profiles and view profiles of other members for making contacts.

This app will be built as a Chrome App so users can run it as a Desktop app or from their web browsers. 

The manifest denotes a background script, main.js,
detailed below:

```javascript
chrome.app.runtime.onLaunched.addListener(function() {
  // Center window on screen.
  var screenWidth = screen.availWidth;
  var screenHeight = screen.availHeight;
  var width = 500;
  var height = 300;

  chrome.app.window.create('index.html', {
    id: "helloWorldID",
    outerBounds: {
      width: width,
      height: height,
      left: Math.round((screenWidth-width)/2),
      top: Math.round((screenHeight-height)/2)
    }
  });
});
```

This simply waits for the launch event for the application (`chrome.app.runtime.onLaunched.addListener`)
and, at that point, creates a window using a basic HTML page, index.html, as the source.

## Resources

* [Runtime](http://developer.chrome.com/apps/app.runtime.html)
* [Window](http://developer.chrome.com/apps/app.window.html)
     
## Screenshot
![screenshot](/samples/hello-world/assets/screenshot_1280_800.png)

