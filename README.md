# console.js
A functioning console polyfill for browsers which don't support console


This project was inspired by [fauxconsole](https://github.com/csanquer/fauxconsole)。


My console.js provides
* console.log/info/warn/error()
* logging before DOM is ready
* using an alias for 'console'
* enforced substitution for builtin console
* a toolbar to hide or clear log content in the simulated console, or close it completely

If you want to log detailed content of an object, you need to `JSON.stringify()` it first, 
using [JSON-js](https://github.com/douglascrockford/JSON-js), or better, 
[my improved fork](https://github.com/xxfcz/JSON-js), which fixed a for-in bug in IE6-8. 


Usage
=====

To reference the simulated console using a name other than traditional `console`, you can provide an alias:

    <script src="lib/console.js"  data-alias="myConsole"></script>

To force the browser to use the simulated console, even if they have builtin implementation, you can do this:

    <script src="/conlibsole.js"  data-forced="true"></script>

