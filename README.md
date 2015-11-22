## What is it?

bootstrapDatepickr is light weight Bootstrap styled datepicker with simple but powerful options. bootstrapDatepickr plays nice on most types of desktop and mobile browsers. The selected date is shown with a "primary" background colour and today's date is shown by a "warning" background colour.

## What does it look like?

Here is a live [Demo](http://mrvautin.github.io/bootstrapDatepickr.html). Try for yourself.

Mobile looks like:

![](http://mrvautin.github.io/images/bootstrapDatepickr-mobileexample-small.jpg)

## Stop. Where can I get it?

Everything can be downloaded from [here](https://github.com/mrvautin/bootstrapDatepickr/archive/master.zip)

## How does it work?

Include both the `dist/bootstrapDatepickr-1.0.0.min.css` and `dist/bootstrapDatepickr-1.0.0.min.js` files.

```javascript
<link rel="stylesheet" href="dist/bootstrapDatepickr-1.0.0.min.css">
<script src="dist/bootstrapDatepickr-1.0.0.min.js"></script>
```

Then add the input element to trigger the datepicker:

```javascript
<input id="bootstrapDatepickr" class="form-control" placeholder="Pick a date">
```

You can also use a bootstrap input-group-addon:

```javascript
<div class="input-group">
	<span class="input-group-addon" id="basic-addon1"><i class="fa fa-calendar"></i></span>
	<input type="text" id="bootstrapDatepickr" placeholder="Pick a date" class="form-control">
</div>
```

Then add the Javascript to target the input element:

```javascript
<script>
	$(document).ready(function() {
		$("#bootstrapDatepickr").bootstrapDatepickr();
	});
</script>
```

## Options

There is currently only one option to format the returned date using `date_format`

Example usage:

```javascript
<script>
	$(document).ready(function() {
		$("#bootstrapDatepickr").bootstrapDatepickr(
			{
				date_format: "d-m-Y"
			}
		);
	});
</script>
```

A list of date format characters is listed below. Note: You can use punctuation to format your date to your liking. Eg: Saturday, 1st of April 2005 would be `l, do of F Y` 

|Character|Description|Example|
|--- |--- |--- |
|d|Day of the month, 2 digits with leading zeros|01 to 31|
|do|The octal day value. Eg: 1st, 2nd, 23rd|1st to 31st|
|D|A textual representation of a day|Mon through Sun|
|j|Day of the month without leading zeros|1 to 31|
|l (lowercase ‘L’)|A full textual representation of the day of the week|Sunday through Saturday|
|w|Numeric representation of the day of the week|0 (for Sunday) through 6 (for Saturday)|
|F|A full textual representation of a month|January through December|
|m|Numeric representation of a month, with leading zero|01 through 12|
|M|A short textual representation of a month|Jan through Dec|
|n|Numeric representation of a month, without leading zeros|1 through 12|
|U|The number of seconds since the Unix Epoch|1413704993|
|y|A two digit representation of a year|99 or 03|
|Y|A full numeric representation of a year, 4 digits|1999 or 2003|