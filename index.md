<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
			embeddedservice_bootstrap.settings.enableUserInputForConversationWithBot = false; // Prevent user from typing if bot hasn't responded.
		
		window.addEventListener("onEmbeddedMessagingReady", () => {            
			console.log( "Inside Prechat API!!" );
			embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( {'QueueName' : 'Sheplers Messaging' } );
			});

			embeddedservice_bootstrap.init(
				'00D6g0000050w0P',
				'Sheplers_Messaging',
				'https://bootbarn.my.site.com/ESWSheplersMessaging1770066250362',
				{
					scrt2URL: 'https://bootbarn.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bootbarn.my.site.com/ESWSheplersMessaging1770066250362/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</html>
