autoStorage
===========
Automatic webstorage for jQuery

**REQUIREMENTS**

You need jQuery to run this plugin. I used jQuery v1.6.4 to develope this plugin, but older versions may handle it too. Your browser needs support for webstorage stuff.

**HOWTO**

Just call autoStorage() on any set of forms (e.g. $('forms').autoStorage();) and the values will be saved in the specified webstorage by submitting the form and reloaded by reloading the page.

**IMPORTANT**

*	Every form needs a unique name.

*	Every element in the form needs a unique name (Except radiobuttons).

*	For element names containing array-brackets, use indeces. (e.g name[1], name[2] ... multipe fields with the same name will cause overwriting data)

**SETTINGS / PARAMETERS**

*	*"storageType" : "local" | "session"*

	Define the type of storage. At the moment there is no support for sqlite (As it is absolutely useless due a lack of support by most browsers).
	The default is "local".
	
*	*"exclude" : ["element1", "element2" ... ]*

	Pass an array with element names to exclude from storage.
	
**EXAMPLE**

	$(document).ready( function() {
		$('form').autoStorage( {
			'storageType' : 'localStorage',
			'exclude' : ['textfield1', 'textfield2]
		});
	});
	