# ios-search
Getting Started with iOS Search

Two types of indexes:

	- A private on-device index. Each device contains a private index whose information is never shared with Apple or synced between devices. When you make an item available in a user’s on-device index, only that user can view the item in search results.

	- Apple’s server-side index. The server-side index stores only publicly available data that you’ve marked appropriately on your website.

NSUserActivity : 

	- Using Handoff
	- if a task can be represented as an NSUserActivity to be handed off to a different device e.g. watch
	- it can be stored in a search index and later continued on the same device.
	- can create a deep linking with safari search using web markup and eligibleForPublicIndexing
	- make app states and navigation points searchable

Core Spotlight :

	- Conventional, Apple only now out in wild
	- Can index virually everything
	- Best way for full search capability
	- don’t use Core Spotlight APIs to make items publicly searchable.
	- make app contents searchable
	- can be done in background (Core Spotlight defines an app extension you can implement to index items when your app isn’t running.)
	
Web markup : 

	- apps that mirror their public content from a web site
	- WWDC app
	- creating Deep Links from app
	- use web markup to let Apple’s web crawler (called Applebot) index your content in Apple’s server-side index and make it available to all iOS users in Spotlight and Safari search results.
	- make website contents searchable, deep linking
	
	- Choosing Search : 
https://developer.apple.com/library/ios/documentation/General/Conceptual/AppSearch/Choosing.html#//apple_ref/doc/uid/TP40016308-CH3-SW1

	- Best Practices: 
https://developer.apple.com/library/ios/documentation/General/Conceptual/AppSearch/SearchUserExperience.html#//apple_ref/doc/uid/TP40016308-CH11-SW1

	- Technical Notes:
https://developer.apple.com/library/prerelease/ios/technotes/tn2416/_index.html
