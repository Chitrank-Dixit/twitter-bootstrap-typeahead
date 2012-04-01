typeahead.js
============

An extension of the Twitter Bootstrap Typeahead plugin (as of v2.0.2)<br />
<http://twitter.github.com/bootstrap/javascript.html#typeahead>

Required
-----------------
* Twitter Bootstrap 2.0.2
* jQuery 1.7.1

About
-----
All the thanks in the world to [@mdo](https://twitter.com/#!/mdo) and [@fat](https://twitter.com/#!/fat) of [@twitter](https://twitter.com/) for the wonderful Bootstrap utility.<br /><br />
I required more functionality out of the typeahead plugin that was included so I created this simple extension.

Changes
-------

**matchProp**<br />
Default: *name*<br />
Usage: The object property to match against.

**sortProp**<br />
Default: *name*<br />
Usage: The object property to use when sorting the items.

**valueProp**<br />
Default: *id*<br />
Usage: The object property to return when an item is selected.

**itemSelected**<br />
Default: *function (item, val, text) {}*<br />
Usage: The callback function that is invoked when an item is chosen.  Takes the element, value as described by *valueProp* and text as described by *textProp* as parameters.

Sample Usage
------------
    var cities = [
			{ID: 1, Name: 'Toronto'},
			{ID: 2, Name: 'Montreal'},
			{ID: 3, Name: 'New York'},
			{ID: 4, Name: 'Buffalo'},
			{ID: 5, Name: 'Boston'},
			{ID: 6, Name: 'Columbus'},
			{ID: 7, Name: 'Dallas'},
			{ID: 8, Name: 'Vancouver'},
			{ID: 9, Name: 'Seattle'},
			{ID: 10, Name: 'Los Angeles'}
	    ]

	$(function() {
		$('#myElement').typeahead({
			source: cities,
			matchProp: 'Name',
			sortProp: 'Name',
			valueProp: 'ID',
			itemSelected: function(val) {
				alert('You selected the city ' + text + ' with ID ' + val)
				console.log(item)
			}
		})
	})

A full working example is included in this project.