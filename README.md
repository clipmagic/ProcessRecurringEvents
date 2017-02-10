# ProcessRecurringEvents V0.0.1


## General information
This module enables you to automatically create pages based on a ProcessWire page template, eg Calender detail page that has calendar event recurrences.

## Installation
* Ensure you've installed the following Core Modules:
	*	FieldtypeDatetime
	*  FieldtypeOptions
	*  FieldtypeCheckbox
	*  ProcessPageClone

* Download the zip file into your site/modules folder then expand the zip file. 
* Next, login to ProcessWire > go to Modules > click "Refresh". You should see a note that a new module was found. Install the ProcessRecurringEvents module. 


## Usage
### Create your fields
* Event start date as type Datetime
* Event end date as type Datetime
* Event Recurring as type Checkbox
* Event number of recurrences as type Text
* Event Interval as type Options - use the PHP time intervals, eg Day, Week, Month, as the single choice options

### Update your template(s)
Add your new fields to your chosen templates(s)

### Configure the module
This module does not automatically create new fields. Instead, you create the fields, or apply ones you're already using in your templates, then map them to the fields needed by this module.

The only field you don't need to create in the module configuration is the Maximum Number of Recurrences. It's just a safeguard so that should an admin save a stupid number in the Event Detail template, this number will override the page number of recurrences.

Strongly recommend that in your template text field for number of recurrences, you use pattern [0-9] and maxlength of 2, ie cannot enter more than 99 recurrences.

### Basic usage
The module autoloads and looks for the templates you've nominated in the module configuration. When it finds a page that has the chosen template & fields and the checkbox field you created for 'Recurring' checkbox ticked, the magic happens.

Once the recurrence pages are created, they're just pages. You can edit, unpublish, etc as you wish. The only thing to note is that should the originating page title be updated, the recurring event page titles will also be updated to match.



## Change log
2017-02-10: Initial release, v0.0.1

