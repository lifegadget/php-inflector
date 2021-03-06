#PHP-Inflector

Converts singular to plural (and back) as well other useful string transforms. This is all based on the English language and was originally sourced from:

> [PHP Class](http://www.kavoir.com/2011/04/php-class-converting-plural-to-singular-or-vice-versa-in-english.html)

The original source appears to be a company called Akelos which offered it as part of their ruby on rails framework. It appears, to have gone out of existance (or at least they've vacated their URL). 
I have simply transposed the code and documentation into a git-friendly way of sharing. 

> **Note**: the code was originally offered under the [**GNU Lesser General Public License**](http://en.wikipedia.org/wiki/GNU_Lesser_General_Public_License) so I think we should proxy that arrangement forward.

## Functions ##

- `Inflector::pluralize`

	return the plural form of the given English word, e.g. “search” to “searches”.	
- `Inflector::singularize` 

	return the singular form of the given English word, e.g. “searches” to “search”

- `Inflector::titleize` 

	create a title text from the given string, e.g. “WelcomePage”, “welcome_page” or “welcome page” to “Welcome Page”.

- `Inflector::pascalize` 

	return the PascalCased text from the given string, e.g. “send_email” to “SendEmail”, “who’s online” to “WhoSOnline”.

- `Inflector::camelize` 

	return the camelCased text from the given string, e.g. “send_email” to “sendEmail”, “who’s online” to “whoSOnline”.

- `Inflector::underscore` 

	return a underscored text from the given string, e.g. “CamelCased” or “ordinary Word” to “underscored_word” that is lowercased.

- `Inflector::humanize` 

	return a human-readable text from the given string, e.g., by replacing underscores with spaces, and by upper-casing the initial character by default.

- `Inflector::variablize` 

	same as camelize but first char is underscored.

- `Inflector::tableize` 
	
	converts a class name to its table name by rails naming conventions.

- `Inflector::classify` 

	converts a table name to its class name by rails naming conventions.


## Example Usage ##

````php
/* Singular to plural / Plural to singular */

echo Inflector::pluralize('search'); //  searches
echo Inflector::singularize('cases'); //  case
echo Inflector::pluralize('query'); //  queries
echo Inflector::singularize('queries'); //  query
echo Inflector::pluralize('ability'); //  abilities
echo Inflector::singularize('abilities'); //  ability
echo Inflector::pluralize('analysis'); //  analyses
echo Inflector::singularize('analyses'); //  analysis
echo Inflector::pluralize('information'); //  information
echo Inflector::singularize('information'); //  information
echo Inflector::pluralize('mouse'); //  mice
echo Inflector::singularize('mice'); //  mouse

/* CamelCase to underscore / underscore to CamelCase */

echo Inflector::underscore('SpecialGuest'); //  special_guest
echo Inflector::underscore('FreeBSD'); //  free_bsd
echo Inflector::underscore('HTML'); //  html
echo Inflector::pascalize('free_bsd'); //  FreeBsd
echo Inflector::pascalize('html-home'); //  HtmlHome
echo Inflector::camelize('free_bsd'); //  freeBsd
echo Inflector::camelize('html-home'); //  htmlHome

/* Underscore to "human-text" / "Human-text" to Underscore */

echo Inflector::humanize('employee_salary'); //  Employee salary
echo Inflector::underscore('Employee salary'); //  employee_salary

/* Examples of titleize() */

echo Inflector::titleize('ActiveRecord'); // Active Record
echo Inflector::titleize('action web service'); // Action Web Service

/* Examples of ordinalize() */

echo Inflector::ordinalize(1); // outputs 1st
echo Inflector::ordinalize(2); // outputs 2nd
echo Inflector::ordinalize(3); // outputs 3rd
echo Inflector::ordinalize(4); // outputs 4th
echo Inflector::ordinalize(5); // outputs 5th
echo Inflector::ordinalize(20); // outputs 20th
echo Inflector::ordinalize(21); // outputs 21st
````

