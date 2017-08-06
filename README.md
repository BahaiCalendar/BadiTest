# BadiTest

Test to support all the projects in the [BahaiCalendar group](https://github.com/BahaiCalendar) so there is no need for redundancy.  All tests are in [JSON](http://www.json.org/) files.

[BahaiCalendar](https://github.com/BahaiCalendar) libraries convert between Gregorian and [Badi / Bahai](https://en.wikipedia.org/wiki/Bah%C3%A1%27%C3%AD_calendar) calendars.

Previously at [BadiCal](https://github.com/dmcblue/BadiCal) but that repo is being split into individual languages in the [BahaiCalendar group](https://github.com/BahaiCalendar).

There are currently versions for:
+ [PHP](https://github.com/BahaiCalendar/BadiCalPHP)
+ [Javascript](https://github.com/BahaiCalendar/BadiCalJS)

## Format
Each file is a group of tests.  The group has a *name*, *description* and an array of *tests*.

Tests have the following format:

```javascript
{
	"name" : "Naw Ruz",
	"description" : "",
	"error" : "",
	"type" : "two-way",
	"input" :{
		"type"  : "Gregorian",
		"year"  : 2015,
		"month" : 3,
		"date"  : 21,
		"daytime" : true
	},
	"output" : {
		"type"  : "Badi",
		"year"  : 172,
		"month" : 1,
		"date"  : 1,
		"daytime" : true
	}
}
```

Test types, etc, will be expanded as needed. Currently, *two-way* is a basic equivalency test.  W is Gregorian, X is Badi; B(W) = Y is Badi, G(X) = Z is Gregorian; Assert W == Z AND X == Y. 