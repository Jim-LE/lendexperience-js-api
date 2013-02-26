lendexperience-js-sdk
=====================

This is the official Javascript SDK for Lend Experience.

````<script type="text/javascript">
  	// Load the SDK Asynchronously
		(function(d){
			var js, id = "libs-le-1.1", ref = d.getElementsByTagName('script')[0];
			if (d.getElementById(id)) {return;}
			js = d.createElement("script");js.id = id;js.async = true;
		    js.src = "//operationwave.elasticbeanstalk.com/WebRoot/Javascript/testjs.js";
			//js.src = "../Tests/testjs.js";
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
	</script>````
