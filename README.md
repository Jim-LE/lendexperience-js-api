lendexperience-js-api
=====================

This is the official Javascript API for Lend Experience. At this time the API supports access to the "content widget."

<h2>Content Widget</h2>

Getting started is quick and easy. The API can be loaded asynchronously by copying and pasting the following code into the HTML on your page.
It is recommended that you place the code within the <BODY> tags, at the top, before all other code with in the body.

You must provide your appID and CommunityID to establish a connection (credentials can be accessed in the API tools section of your
Lend Experience admin page).

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
