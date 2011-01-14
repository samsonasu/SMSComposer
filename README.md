# PhoneGap SMSComposer #
by Grant Sanders

## Adding the Plugin to your project ##

Using this plugin requires [PhoneGap for iPhone](http://github.com/phonegap/phonegap-iphone).

1. Add the SMSComposer.h and SMSComposer.m files to your "Plugins" folder in your PhoneGap project
2. Add the SMSComposer.js files to your "www" folder on disk, and add a reference to the .js file after phonegap.js.

## RELEASE NOTES ##

### 201101112 ###
* Initial release
* Adds SMS text message composition in-app.
* Requires iOS 4.0 or higher. 
  Attempts to compose SMS text without running 4.0+ fails gracefully with a friendly message.

## EXAMPLE USAGE ##

* All parameters are optional.
window.plugins.smsComposer.showSMSComposer();


* Passing phone number and message.
window.plugins.smsComposer.showSMSComposer('3424221122', 'hello');

* Multiple recipents are separated by comma(s).
window.plugins.smsComposer.showSMSComposer('3424221122,2134463330', 'hello');


* showSMSComposerWithCB takes a callback as its first parameter.  
* 0, 1, 2, or 3 will be passed to the callback when the text message has been attempted.
window.plugins.smsComposer.showSMSComposerWithCB(function(result){

	if(result == 0)
		alert("Cancelled");
	else if(result == 1)
		alert("Sent");
	else if(result == 2)
		alert("Failed.");
	else if(result == 3)
		alert("Not Sent.");		

},'3424221122,2134463330', 'hello');


* A fully working example as index.html has been added to this repository.

## LICENSE ##

The MIT License

Copyright (c) 2010 Grant Sanders

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

