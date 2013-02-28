lendexperience-js-api
=====================

This is the official Javascript API for Lend Experience. At this time the API supports access to the "content widget."

<h2>Getting Started</h2>

Getting started is quick and easy. The API can be loaded asynchronously by copying and pasting the following code into the HTML on your page.
It is recommended that you place the code within the BODY tags, before all other code within the body, inorder to optimize performance of the API.

You must provide your API Access Keys(appID and CommunityID) to establish a connection (Keys can be accessed in the API tools section of your
Lend Experience admin page). Access to the API is restricted to verified domains. If you currently possess API Access Keys then your domain 
is most likely verified.

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

The content widget provides a customizable stream of experiences, opportunities and questions that can be embedded directly into your site.
To set-up the content widget place the following DIV tag where you would like the "content widget" to appear on your page:
````
<div id="le-root">
</div>

````
The "le-root" DIV is the container for the content widget. Once the API has been asynchronously loaded it will detect the 
existence of the "le-root" DIV. It will then load the content widget inside of the "le-root" DIV. The "le-root" DIV
can be styled, but keep in mind that the loaded "content widget" will have a minimum width of 300px.

Live Example of the "Content Widget"
<a href="https://lendexperience.com/widget/example">https://lendexperience.com/widget/example</a>

Questions?
Send an email to <a href="mailto:jim@lendexperience.com">jim@lendexperience.com</a>.

Visit Us:
<a href="https://lendexperience.com/le">https://lendexperience.com</a>
