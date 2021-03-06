# CookLine for Android (using PhoneGap)

Using PhoneGap for Android, wraps CookLine, a web sample app that allows you to publish back to your Facebook Timeline about what you're eating, using Open Graph.

This sample code is the completed sample Android code that was presented at [AnDevCon III 2012](http://www.andevcon.com/AndevCon_III/index.html).

Authors: Christine Abernathy (caabernathy)

## Installing

This section will walk you through the following:

* Getting Started
* Native SDK Integration Demo
  * Creating your Facebook app
  * Installing the Android app
* Apache Cordova/PhoneGap Integration Demo
  * Install the CookLine Web App
  * Installing the Android app

### Getting Started

Your install package should have the following files:

* NativeSDK Android Project

* WebCordova Android Project


To get the sample code do the following:

* Install [Git](http://git-scm.com/).

* Pull the samples package from GitHub:

    git clone git://github.com/fbsamples/android-integration-sdk-phonegap


### Creating your Facebook app (Native SDK Demo)

First set up a Facebook app using the Developer app:

* Create a new [Facebook app](https://developers.facebook.com/apps)
* (Optional) Enter the `App Namespace` when creating your app. You can choose a simple string to identify your app, such as ''awesomeapp'', but it must be unique.
* Configure the Native Android App settings.
  * Enable the _Configured for Android SSO_ setting.
  * Enter you app's signature in the _Android Key Hash_ field. For more information see the [Android Tutorial](https://developers.facebook.com/docs/mobile/android/build/#sig).
  * Enter "com.facebook.samples.myapp" in the _Android Package Name_ setting.
  * Enter "com.facebook.samples.myapp.App" in the _Android Class Name_ setting.
  * Enter a value for the _Android Market URI_. The value must correspond to any valid Google Play URL.



### Installing the Android app (Native SDK Demo)

1. Get the latest Facebook Android SDK from GitHub: git clone git://github.com/facebook/facebook-android-sdk.git

1. Launch Eclipse

1. Create a Facebook Android SDK Project:
   1. From the Eclipse menu, navigate to File > New > Android Project
   1. Select "Create project from existing source"
   1. The Facebook Android SDK package should include a folder, facebook-android-sdk/facebook
   1. Browse to the facebook folder and select it
   1. Click Next
   1. Select Android 2.2 as the Build Target
   1. Click Finish

1. Import the sample app:
   1. From the Eclipse menu, navigate to File > Import
   1. Select General > Existing Projects into Workspace
   1. The sample package should include a folder, NativeSDK
   1. Browse to the NativeSDK folder and select it
   1. Click Finish

1. Include the Facebook Android SDK:
   1. From the Eclipse Package Explorer, select the NativeSDK project
   1. Right-click and select the Properties menu
   1. In the Library section, click Add
   1. Select com_facebook_android
   1. Click OK
   1. Click OK to exit the Properties dialog

1. Set up your App ID:
   1. From the Eclipse Package Explorer, select the NativeSDK project
   1. Open up App.java (under the src/com.facebook.samples.myapp folder)
   1. Change the existing app ID:

             public static final String APP_ID = "321416411224717";

     to:

             public static final String APP_ID = "YOUR_APP_ID";

1. Install the Facebook app. Go to the [Android Tutorial](https://developers.facebook.com/docs/mobile/android/build/#install) to find more instructions on this.

1. Run the application as an Android Application. If you have any issues check out the [Android Tutorial](https://developers.facebook.com/docs/mobile/android/build/).


### Install the CookLine Web App

Follow the [CookLine app](https://github.com/fbsamples/CookLine) install instructions. Note your app's domain, namespace, and app Id. You will use this to configure your app in the next section.

### Installing the Android app (Apache Cordova Demo)

1. Get the latest Facebook Android SDK from GitHub, if not previously cloned: git clone git://github.com/facebook/facebook-android-sdk.git

1. Download the latest Apache Cordova (PhoneGap) build from [www.phonegap.com/download](www.phonegap.com/download)

1. Get the latest Apache Cordova Facebook Connect Plugin from GitHub: git clone https://github.com/davejohnson/phonegap-plugin-facebook-connect.git

1. Get the latest Facebook Android SDK from GitHub: git clone git://github.com/facebook/facebook-android-sdk.git

1. Launch Eclipse

1. Create a Facebook Android SDK Project if you have done so previously.

1. Import the sample app:
   1. From the Eclipse menu, navigate to File > Import
   1. Select General > Existing Projects into Workspace
   1. The sample package should include a folder, WebCordova
   1. Browse to the WebCordova folder and select it
   1. Click Finish

1. Include the Facebook Android SDK:
   1. From the Eclipse Package Explorer, select the WebCordova project
   1. Right-click and select the Properties menu
   1. In the Library section, click Add
   1. Select com_facebook_android
   1. Click OK
   1. Click OK to exit the Properties dialog

1. Edit the CookLine web files - beef_curry.html, lasagne.html, pizza.html:
   1. Change occurrences of ''294113397324835'' to ''YOUR_APP_ID''
   1. Change occurrences of ''cookline.herokuapp.com'' to your domain
   1. Change occurrences of ''cookline:'' to ''YOUR_APP_NAMESPACE:''

1. Install Cordova libraries, scripts:
   1. Copy &lt;CORDOVA-INSTALL>/lib/android/cordova-1.7.0.jar to the WebCordova project _libs_ folder
   1. Copy &lt;CORDOVA-INSTALL>/lib/android/cordova-1.7.0.js to the WebCordova project _assets/www_ folder
   1. Copy &lt;CORDOVA-INSTALL>/lib/android/xml to the WebCordova project res folder

1. Install Apache Cordova Facebook Connect Plugin libraries, scripts:
   1. Copy &lt;PLUGIN-INSTALL>/www/cdv-plugin-fb-connect.js to the WebCordova project _assets/www_ folder
   1. Copy &lt;PLUGIN-INSTALL>/lib/facebook_js_sdk.js to the WebCordova project _assets/www_ folder
   1. Copy &lt;PLUGIN-INSTALL>/native/android/src/org to the WebCordova project _src_ folder

1. Run the application as an Android Application. If you have any issues check out the [Android Tutorial](https://developers.facebook.com/docs/mobile/android/build/).

## Contributing

All contributors must agree to and sign the [Facebook CLA](https://developers.facebook.com/opensource/cla) prior to submitting Pull Requests. We cannot accept Pull Requests until this document is signed and submitted.

## License

Copyright 2012-present Facebook, Inc.

You are hereby granted a non-exclusive, worldwide, royalty-free license to use, copy, modify, and distribute this software in source code or binary form for use in connection with the web services and APIs provided by Facebook.

As with any software that integrates with the Facebook platform, your use of this software is subject to the Facebook Developer Principles and Policies [http://developers.facebook.com/policy/]. This copyright notice shall be included in all copies or substantial portions of the software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.