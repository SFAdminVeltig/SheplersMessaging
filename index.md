<html>
<script type='text/javascript'>
	function initEmbeddedMessaging() {
		try {
			embeddedservice_bootstrap.settings.language = 'en_US'; // For example, enter 'en' or 'en-US'
			
		window.addEventListener("onEmbeddedMessagingReady", () => {            
			console.log( "Inside Prechat API!!" );
			embeddedservice_bootstrap.prechatAPI.setHiddenPrechatFields( {'QueueName' : 'Sheplers Messaging' } );
			});
			window.addEventListener("onEmbeddedMessagingReady", e => {
			    embeddedservice_bootstrap.prechatAPI.setVisiblePrechatFields({
			        "_firstName": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "_lastName": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "_email": {
			            "value": "",
			            "isEditableByEndUser": true
			        },
			        "Prechat_Choice": {
			            "value": "",
			            "isEditableByEndUser": true
				}
			    });
			});
			embeddedservice_bootstrap.init(
				'00DOt000002m0EL',
				'Sheplers_Messaging',
				'https://bootbarn--uat.sandbox.my.site.com/ESWSheplersMessaging1770066250362',
				{
					scrt2URL: 'https://bootbarn--uat.sandbox.my.salesforce-scrt.com'
				}
			);
		} catch (err) {
			console.error('Error loading Embedded Messaging: ', err);
		}
	};
</script>
<script type='text/javascript' src='https://bootbarn--uat.sandbox.my.site.com/ESWSheplersMessaging1770066250362/assets/js/bootstrap.min.js' onload='initEmbeddedMessaging()'></script>
</html>
