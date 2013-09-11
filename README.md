#µXHR

The teeny tiny XHR library.

##Usage

```js
// with a data object
var data = { foo: 'bar', baz: 5 };
var options = {
	complete: function (response) { ... }
};

uxhr('endpoint.php', data, options);

// ... or with a data string
var data = 'war=peace&freedom=slavery&ignorance=strength';
var options = {
	complete: function (response) { ... }
};

uxhr('endpoint.php', data, options);
```

##Arguments

| Argument		| Type				| Required		|
|---------------|-------------------|---------------|
| url			| String			| Yes			|
| data			| String | Object	| No			|
| options		| Object			| No			|

##Options

| Option		| Type		| Default		| Notes									|
|---------------|-----------|---------------|---------------------------------------|
| method		| String	| `GET`			| `GET`, `POST`, `PUT`, `DELETE`, etc.	|
| headers		| Object	| {}			| Custom headers for this request		|
| timeout		| Number	| 0				| Timeout (in ms) before aborting the request |
| complete		| Function	| function(){}	| A callback fired when the request is completed |
| success		| Function	| function(){}	| A callback fired when the request is completed successfully (eg. with HTTP status code < 400) |
| error			| Function	| function(){}	| A callback fired when the request returns an error (eg. HTTP status code >= 400) |

##Browser support