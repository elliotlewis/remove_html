Remove HTML tags - EE Plugin
=======================================

 * Author:					[Elliot Lewis](http://notwothesame.com)
 * Repro on GitHub:			[GitHub.com](https://github.com/elliotlewis/remove_html)
 * Product Page on Devot-ee:	[Devot-ee.com](http://devot-ee.com/add-ons/remove_html)


Version History
---------------
 * __1.0, 17/12/2012__  
    1st release. EE1 and EE2 versions.


Requirements
------------

 * PHP5+
 * ExpressionEngine 2.4 or later.
 * ExpressionEngine 1.7.x


Description
-----------
Expression engine Add-on to remove all HTML tags from text. Specifically it removes any text in the format <tag> or </tag>. So any text in that format will be removed even if it's not a valid HTML tag.


Usage
-----

### Example ###
Setting up a field type with 'Text Formatting' of 'XHTML' to preserve line-breaks. When displayed in a template the correct HTML will output with the content. It is not possible to choose the formatting of this field via template tags.

If you need to use the field data in a form field, eg. textarea you would not want the HTML code to display as well. This Add-on removes the formatting when displayed in template (original formatting is preserved in EE).

Eg. This:

 	<p>Some content in a field, added via the CP.<br>A new line of text.</p>

Outputs as:

	Some content in a field, added via the CP.
	A new line of text.

### Template Tags ###
Assuming you have named your field 'my_field' as a custom field and the Text Formatting is set to anything other than 'none'.

	{exp:remove_html}
	{my_field}
	{/exp:remove_html}


Usage
-----

### Installation ###

#### EE 2 ####

Add 'remove_html' folder to system > third_party folder

#### EE 1 ####

Place 'pi.remove_html.php' in to the system > plugins folder
