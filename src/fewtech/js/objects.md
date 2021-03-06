# Objects

Objects are a built in data type. An Object is a collection of
**properties**(variables) and **methods**(functions), which are called **members** of the
Object. 

We have already looked at 2 built in
objects -- Strings and Arrays. They both have property `length` and many
different methods. 

Object property and methods can be accessed via the dot (`.`) operator
or through box brackets (`[]`). For example the string property `length`
can be accessed as follows:

```js
var s = "a test string";
var len = s.length; // using dot operator
var len = s["length"]; // using box brackets
```

Similarly any methods (say `indexOf()`) can be accessed similarly:

```js
var s = "a test string";
var pos = s.indexOf(a); // using dot operator
var pos = s["indexOf"](a); // using box brackets
```


## Object Syntax

```js
var obj = { property_1:   value_1,   // property_# may be an identifier...
            2:            value_2,   // or a number...
            // ...,
            'property n': value_n }; // or a string
```

## Built In Objects

In this section we look at more built in objects.

### The `Object` Object

There is a built-in Object called `Object`. This has one useful static
method that we will discuss here. `Object.keys()` returns the list of
all the objects member keys. It is very handy when you want to iterate
the Object.

```js
var keys = Object.keys(location) // can be used to get keys on any object

for(var i = 0; i < keys.length; i++){
  console.log("Key: " +keys[i]);
  console.log("Key value: " + location[keys[i]]);
}
```

### The `Date` Object
The `Date` object provides an easy way to store and manipulate dates in
JS.

Each `Date` object stores a particular date and time. Initializing a
`Date` object without arguments will give you the current date-time.

```js
var now = new Date();
```

<div class='notes'>

#### The <code>new</code> keyword

The `new` keyword is used to create a new object. Notice that we did not
use `new()` to create Arrays and Strings. That is because they are
built-in objects which can be instantiated without `new`(although you
could if you choose to).
</div>


As an object `Date()` has built in methods[<a
href='../../bib.html#javascript---the-date-object---tutorialspoint-tutorialspointcom'>Ref</a>]:

<div style='overflow:auto'>

<table>
<tbody><tr>
<th style="text-align:center;">Method 
</th><th>
Description</th></tr>
<tr>

<td><code>Date()</code>
</td><td>
<p>Gets today's date and time</p></td>
</tr>
<tr>

<td><code>getDate()</code>
</td><td>
<p>Gets the day of the month for the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getDay()</code>
</td><td>
<p>Gets the day of the week for the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getFullYear()</code>
</td><td>
<p>Gets the year of the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getHours()</code>
</td><td>
<p>Gets the hour in the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getMilliseconds()</code>
</td><td><p>Gets the milliseconds in the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getMinutes()</code>
</td><td><p>Gets the minutes in the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getMonth()</code>
</td><td><p>Gets the month in the specified date according to local time.</p></td>
</tr>
<tr>

<td><code>getSeconds()</code>
</td><td><p>Gets the seconds in the specified date according to local time.</p></td>
</tr>
<tr>
<td><code>getTime()</code>
</td><td><p>Gets the numeric value of the specified date as the number of milliseconds since January 1, 1970, 00:00:00 UTC.</p></td>
</tr>
<tr>

<td><code>getTimezoneOffset()</code>
</td><td><p>Gets the time-zone offset in minutes for the current locale.</p></td>
</tr>
<tr>

<td><code>getUTCDate()</code>
</td><td><p>Gets the day (date) of the month in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCDay()</code>
</td><td><p>Gets the day of the week in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCFullYear()</code>
</td><td><p>Gets the year in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCHours()</code>
</td><td><p>Gets the hours in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCMilliseconds()</code>
</td><td><p>Gets the milliseconds in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCMinutes()</code>
</td><td><p>Gets the minutes in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCMonth()</code>
</td><td><p>Gets the month in the specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>getUTCSeconds()</code>
</td><td><p>Gets the seconds in the specified date according to universal time.</p></td>
</tr>
<tr>
<td><code>getYear()</code>
</td><td><p><b>Deprecated</b> - Gets the year in the specified date according to local time. Use getFullYear instead.</p></td>
</tr>
<tr>

<td><code>setDate()</code>
</td><td><p>Sets the day of the month for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setFullYear()</code>
</td><td><p>Sets the full year for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setHours()</code>
</td><td><p>Sets the hours for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setMilliseconds()</code>
</td><td><p>Sets the milliseconds for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setMinutes()</code>
</td><td><p>Sets the minutes for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setMonth()</code>
</td><td><p>Sets the month for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setSeconds()</code>
</td><td><p>Sets the seconds for a specified date according to local time.</p></td>
</tr>
<tr>

<td><code>setTime()</code>
</td><td><p>Sets the Date object to the time represented by a number of milliseconds since January 1, 1970, 00:00:00 UTC.</p></td>
</tr>
<tr>

<td><code>setUTCDate()</code>
</td><td><p>Sets the day of the month for a specified date according to universal time.</p></td>
</tr>
<tr>
<td><code>setUTCFullYear()</code>
</td><td><p>Sets the full year for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setUTCHours()</code>
</td><td><p>Sets the hour for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setUTCMilliseconds()</code>
</td><td><p>Sets the milliseconds for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setUTCMinutes()</code>
</td><td><p>Sets the minutes for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setUTCMonth()</code>
</td><td><p>Sets the month for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setUTCSeconds()</code>
</td><td><p>Sets the seconds for a specified date according to universal time.</p></td>
</tr>
<tr>

<td><code>setYear()</code>
</td><td><p><b>Deprecated - </b> Sets the year for a specified date according to local time. Use setFullYear instead.</p></td>
</tr>
<tr>

<td><code>toDateString()</code>
</td><td><p>Gets the "date" portion of the Date as a human-readable string.</p></td>
</tr>
<tr>

<td><code>toGMTString()</code>
</td><td><p><b>Deprecated - </b> Converts a date to a string, using the Internet GMT conventions. Use toUTCString instead.</p></td>
</tr>
<tr>

<td><code>toLocaleDateString()</code>
</td><td><p>Gets the "date" portion of the Date as a string, using the current locale's conventions.</p></td>
</tr>
<tr>
<td><code>toLocaleFormat()</code>
</td><td><p>Converts a date to a string, using a format string.</p></td>
</tr>
<tr>

<td><code>toLocaleString()</code>
</td><td><p>Converts a date to a string, using the current locale's conventions.</p></td>
</tr>
<tr>

<td><code>toLocaleTimeString()</code>
</td><td><p>Gets the "time" portion of the Date as a string, using the current locale's conventions.</p></td>
</tr>
<tr>

<td><code>toSource()</code>
</td><td><p>Gets a string representing the source for an equivalent Date object; you can use this value to create a new object.</p></td>
</tr>
<tr>

<td><code>toString()</code>
</td><td><p>Gets a string representing the specified Date object.</p></td>
</tr>
<tr>

<td><code>toTimeString()</code>
</td><td><p>Gets the "time" portion of the Date as a human-readable string.</p></td>
</tr>
<tr>

<td><code>toUTCString()</code>
</td><td><p>Converts a date to a string, using the universal time convention.</p></td>
</tr>
<tr>

<td><code>valueOf()</code>
</td><td><p>Gets the primitive value of a Date object.</p></td>
</tr>
</tbody></table>

</div>




In Addition there are 2 static `Date()` methods[<a
href='../../bib.html#javascript---the-date-object---tutorialspoint-tutorialspointcom'>Ref</a>]:

<div style='overflow:hidden'>

<table>
<tbody><tr>
<th style="text-align:center;">Method 
</th><th>
 Description</th>
</tr>
<tr>

<td><code>Date.parse()</code>
</td><td><p>Parses a string representation of a date and time and returns the internal millisecond representation of that date.</p></td>
</tr>
<tr>

<td><code>Date.UTC()</code>
</td><td><p>Gets the millisecond representation of the specified UTC date and time.</p></td>
</tr>
</tbody></table>


</div>

### `window` Object (browser only)

For browser based JS, the `window` is the topmost object. All other
objects and variables are derived from the `window` object.

 <img style="display:block;margin:auto" src='../../imgs/windowObject.png'>    
 <figcaption> Fig: 6.5.1 <code>window</code> Object</figcaption>               

Therefore when we write `console.log()` it is interpreted as
`window.console.log()`.

The window object encapsulates other important objects such as --
`location` (which has useful members such as `location.href`,
`location.hash`, `location.host`,  `location.reload()` etc.) and
`document`.
 
### `document` Object (browser only)

<div class='notes'>

#### Document Object Model (DOM)

The Document Object Model (DOM) is the represenation of the HTML document
within JS. The DOM has an *object* associated with each *element* (tag) within
the HTML document. The corresponding object can be used to read tag information (query
status of attributes and their values) as well as set
tag attribute values. Thus a DOM provides a way to read attribute values
from tags (including CSS declarations, since `style` is an attribute)
and set them.


</div>

The `document` Object has important DOM access methods such as
`document.getElementById()`, `document.getElementsByTagName()` ,
`document.getElementsByClassName()`  etc


<div class='notes'>

#### What about jQuery?
jQuery is a wrapper that implements different functions on top of JS.
The main dollar function (`$()`) in jQuery internally uses the DOM
(`document` Object, more specifically the `document.querySelectorAll()`
function).

</div>





