Cordova Plugin for OpenTok Android, iOS
===

Weave video chat into your web (and now mobile!) application.

## Using Cordova CLI
Make sure You have Cordova 3.5.0 Installed. If you haven't, view [Cordova instructions](http://cordova.apache.org/docs/en/3.5.0/guide_cli_index.md.html) Page.  
[Bug filed](https://issues.apache.org/jira/browse/CB-6500) against Cordova.  

Clone this repo to get the source code for OpenTok's Cordova plugin

1. Create a Cordova app by typing into Terminal:  
`cordova create my-app`  

2. Install OpenTok plugin into your app:
`cd my-app`  
`cordova plugin add https://github.com/HanWenDong/OpentokCordovaPlugin.git`  
> Plugin already exists? To remove OpenTokPlugin: `cordova plugin remove com.tokbox.cordova.opentok`

3a. For **Android Apps**, add Android platform into your cordova app
`cordova platform add android`

3b. For **iOS Apps**, add iOS platform into your cordova app  
`cordova platform add ios`  
  iOS deloyment, as of March 14, needs additional setup. See [FAQ/Troubleshoot](https://github.com/songz/cordova-plugin-opentok#faq-troubleshoot-guide).

4. Edit your code in the created `www` folder

5. To deploy your app to your android device:
`cordova run android --device`

6. To deploy your app to your iOS device:  
> As of 1/17/2014, you cannot deploy to device with Cordova CLI for iOS apps. You need to first prepare you iOS app: `cordova prepare iOS`  
> Next, open the project in xcode and run it on device: `open platforms/ios/HelloWorld.xcodeproj`

---

## Getting Started on your Project:
All your editing will be done in your www folder.

To use the opentok library, make sure you include **opentok.js** file in your HTML document.  
` <script type="text/javascript" charset="utf-8" src="opentok.js"></script>`

All JavaScript code should be written in `deviceready` function in */js/index.js* because it is executed after all dependencies has loaded.

    deviceready: function() {
        // Do Your Stuff Here!
    },

To view and interact with elements on the browser console, use [weinre](http://people.apache.org/~pmuellr/weinre/docs/latest/). Here's a few things to take note of if you are using weinre on a local network:
* make sure all devices are connected to the same network
* make sure you bind weinre to 0.0.0.0 so your mobile devices: `weinre --boundHost 0.0.0.0`
* when you include the js library from weinre, make sure to use your computer's ip address and not localhost!

---

## Sample code
Located in `example/www`. To see the interop between mobile and web, simply deploy to your device and visit `https://opentokrtc.com/cordova` on your browser. 

All of the code resides in `example/www/index.html` and `example/www/js/index.js`.  

Have Fun!

----

License
===

Copyright (c) 2014 TokBox, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:


The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

The software complies with Terms of Service for the OpenTok platform described in <http://www.tokbox.com/termsofservice>.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
