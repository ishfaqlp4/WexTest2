<html>
	<head>
		<meta name="viewport" content="width=device-width, initial-scale=1, minimum-scale=1">
		
	</head>
 <body>
	<style>
		.embeddedServiceHelpButton .helpButton .uiButton {
		background-color: #005290;
		font-family: "Arial", sans-serif;
	}
	.embeddedServiceHelpButton .helpButton .uiButton:focus {
		outline: 1px solid #005290;
	}
	</style>
<script type='text/javascript' src='https://c.la3-c1-ia6.salesforceliveagent.com/content/g/js/59.0/deployment.js'></script>
<script type='text/javascript'>
liveagent.init('https://d.la3-c1-ia6.salesforceliveagent.com/chat', '572Ho000000kl8b', '00DHo000002Eet5');
</script>
<script type='text/javascript' src='https://service.force.com/embeddedservice/5.0/esw.min.js'></script>
<script type='text/javascript'>
	var initESW = function(gslbBaseURL) {
		embedded_svc.settings.displayHelpButton = true; //Or false
		embedded_svc.settings.language = ''; //For example, enter 'en' or 'en-US'

		//embedded_svc.settings.defaultMinimizedText = '...'; //(Defaults to Chat with an Expert)
		//embedded_svc.settings.disabledMinimizedText = '...'; //(Defaults to Agent Offline)

		//embedded_svc.settings.loadingText = ''; //(Defaults to Loading)
		//embedded_svc.settings.storageDomain = 'yourdomain.com'; //(Sets the domain for your deployment so that visitors can navigate subdomains during a chat session)

		// Settings for Chat
		//embedded_svc.settings.directToButtonRouting = function(prechatFormData) {
			// Dynamically changes the button ID based on what the visitor enters in the pre-chat form.
			// Returns a valid button ID.
		//};
		//embedded_svc.settings.prepopulatedPrechatFields = {}; //Sets the auto-population of pre-chat form fields
		//embedded_svc.settings.fallbackRouting = []; //An array of button IDs, user IDs, or userId_buttonId
		//embedded_svc.settings.offlineSupportMinimizedText = '...'; //(Defaults to Contact Us)
		  
//manually adding coupon cookies to the site
    //document.cookie = "wex_cc_session=H1F|W7CP|EDH4|M41728";
    document.cookie = "wex_cc_persistent=H1F|W7CP|EDH4|M41728";


var x = document.cookie;
var cookieValue='';
    console.log(x);
		  x.split(';').forEach(function(el) {
     
		     var y = el.split('=');
		     console.log(y);
		      console.log(y[1]);
		     // cookieValue[y[0].trim()] = y[1];
       		if( y[0].trim()==='wex_cc_persistent'){
		       	if(y[1]){
		     		 cookieValue = y[1].split('|')[0];
		       	}
      
      		}
		if(y[0].trim()==='wex_cc_session') {
 		if(y[1]){
     		 	cookieValue = y[1].split('|')[0];
      		 }
		}
 	  console.log(cookieValue);
	});
      console.log(cookieValue);
		
		embedded_svc.settings.extraPrechatFormDetails = [{
  		"label": "visitor URL",
  		"value": cookieValue,
  		"displayToAgent": true,
  		"transcriptFields" : ["Cookie_Value__c"]
		}
 ];
		embedded_svc.settings.enabledFeatures = ['LiveAgent'];
		embedded_svc.settings.entryFeature = 'LiveAgent';

		embedded_svc.init(
			'https://atg37-dev-ed.develop.my.salesforce.com',
			'https://atg37-dev-ed.develop.my.salesforce-sites.com/liveAgentSetupFlow',
			gslbBaseURL,
			'00DHo000002Eet5',
			'Chat_Team',
			{
				baseLiveAgentContentURL: 'https://c.la3-c1-ia6.salesforceliveagent.com/content',
				deploymentId: '572Ho000000kl8b',
				buttonId: '573Ho000000klAw',
				baseLiveAgentURL: 'https://d.la3-c1-ia6.salesforceliveagent.com/chat',
				eswLiveAgentDevName: 'Chat_Team',
				isOfflineSupportEnabled: true
			}
		);
	};

	if (!window.embedded_svc) {
		var s = document.createElement('script');
		s.setAttribute('src', 'https://atg37-dev-ed.develop.my.salesforce.com/embeddedservice/5.0/esw.min.js');
		s.onload = function() {
			initESW(null);
		};
		document.body.appendChild(s);
	} else {
		initESW('https://service.force.com');
	}
</script>
</body>
</html>
