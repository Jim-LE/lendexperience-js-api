lendexperience-js-api
=====================

This is the official Javascript API for Lend Experience. At this time the API supports access to the "content widget."

<h2>Getting Started</h2>

Getting started is quick and easy. The API can be loaded asynchronously by copying and pasting the following code into the HTML on your page.
It is recommended that you place the code within the BODY tags, before all other code within the body, inorder to optimize perforamnce of the API.

You must provide your API Access Keys(appID and CommunityID) to establish a connection (Keys can be accessed in the API tools section of your
Lend Experience admin page). Access to the API is restricted to verified domains. If you currently possess API Access Keys then your domain 
has most likely been verified.

````
<script type="text/javascript">
  	// Load the SDK Asynchronously
		(function(d){
			var js, id = "libs-le-1.1", ref = d.getElementsByTagName('script')[0];
			if (d.getElementById(id)) {return;}
			js = d.createElement("script");js.id = id;js.async = true;
		    	js.src = "//lendexperience.com/API/le-min-v1.1.js";
		    	ref.parentNode.insertBefore(js, ref);
		}(document));
		// Initialize Access to LE
		window.leAsyncInit = function() {
			lendexperience.init({
				appID:         <YOUR APP ID HERE>,
				communityID:  '<YOUR COMMUNITY ID HERE>',
				itemType:      1
			})
		};
</script>
````

<h2>Content Widget</h2>

The content widget provides a customizable stream to experiences, opportunities and requests posted on Lend Experience.
To set-up the content widget place the following <DIV> where you would like the "content widget" to appear on your page:
````
<div id="le-root">
</div>

````
The "le-root" div is the container for the content widget. Once the API has been asynchronously loaded it will detect the 
existence of the "le-root" div. It will then load the content widget inside of the "le-root" div. The "le-root" div
can be styled, but keep in mind that the loaded "content widget" will have a minimum width of 300px.

Questions?
Send an email to <a href="mailto:jim@lendexperience.com">jim@lendexperience.com</a>.

Visit Us:
<a href="https://lendexperience.com/le">https://lendexperience.com</a>
