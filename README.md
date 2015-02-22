# team11
Application for *Hack like a Girl* at Nike WHQ, Feb 2015




<a target="_blank" href="https://chrome.google.com/webstore/detail/nmfpplkdkcbhediajmbhljkafnlahcda">![Try it now in CWS](https://raw.github.com/GoogleChrome/chrome-app-samples/master/tryitnowbutton.png "Click here to install this sample from the Chrome Web Store")</a>


# REACH

REACH is a web application designed as a portal to help women who want to improve their tech skills find mentors and other women with similar interests. Members can create online profiles, view profiles of other members and contact members to iniatiate a professional and/or mentoring connection. 

The app will use existing APIs to make it easier for users to access resources, make personal connections and serve as a "one stop shop" for helping women in tech build their careers. 

We have set up a Chrome App framework to make the app deployable to multiple platforms and leverage existing team skills, but are open to suggestions as to other ways to accomplish this. 

For Chrome App - 
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

![screenshot](https://github.com/infomaven/team11/blob/master/SCREENSHOTS/330x550-homepage.png)
![screenshot](https://github.com/infomaven/team11/blob/master/SCREENSHOTS/330x550-contact-card.png)

