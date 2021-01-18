# “The Past, Present, and Future of Local Storage for Web Applications”
*The simplest choice is JavaScript variables. It may be practical to create a single global variable to store application data, e.g.*

### The advantages of JavaScript variables:

*the fastest and simplest solution
no need to serialize or de-serialize data
ideal for single-page applications
The disadvantages:*

*very fragile — linking elsewhere, refreshing or closing the tab will wipe all data
global variables can be overwritten and analyzed by third-party scripts.*

# window.name (Past and Present)
*The window.name property is a little odd. You can set a single string value which persists between browser refreshes or linking elsewhere and clicking back, e.g.*

# The advantages of window.name:

* simple to use
* data is retained on the client only and never sent to the server
* the property permits several megabytes of information
* wide browser support

# The disadvantages:
* data is lost when the tab or browser is closed
* only a single string value can be stored — serialization will be necessary
* pages in other domains can read or change window.name data — never use it for sensitive information

*window.name was never designed for data storage. It’s a hack and vendors could drop support at any time. For that reason, it’s best to use alternative storage options although the technique has been adopted within legacy browser shims and polyfills.*
