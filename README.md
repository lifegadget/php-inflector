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

- `Inflector::camelize` 

	return the CamelCased text from the given string, e.g. “send_email” to “SendEmail”, “who’s online” to “WhoSOnline”.

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

echo Inflector::pluralize('search'); // outputs searches
echo Inflector::singularize('cases'); // outputs case
echo Inflector::pluralize('query'); // outputs queries
echo Inflector::singularize('queries'); // outputs query
echo Inflector::pluralize('ability'); // outputs abilities
echo Inflector::singularize('abilities'); // outputs ability
echo Inflector::pluralize('analysis'); // outputs analyses
echo Inflector::singularize('analyses'); // outputs analysis
echo Inflector::pluralize('information'); // outputs information
echo Inflector::singularize('information'); // outputs information
echo Inflector::pluralize('mouse'); // outputs mice
echo Inflector::singularize('mice'); // outputs mouse

/* CamelCase to underscore / underscore to CamelCase */

echo Inflector::underscore('SpecialGuest'); // outputs special_guest
echo Inflector::camelize('special_guest'); // outputs SpecialGuest
echo Inflector::underscore('FreeBSD'); // outputs free_bsd
echo Inflector::camelize('free_bsd'); // outputs FreeBsd
echo Inflector::underscore('HTML'); // outputs html
echo Inflector::camelize('html'); // outputs Html

/* Underscore to "human-text" / "Human-text" to Underscore */

echo Inflector::humanize('employee_salary'); // outputs Employee salary
echo Inflector::underscore('Employee salary'); // outputs employee_salary

/* Examples of titleize() */

echo Inflector::titleize('ActiveRecord'); // outputs Active Record
echo Inflector::titleize('action web service'); // outputs Action Web Service

/* Examples of ordinalize() */

echo Inflector::ordinalize(1); // outputs 1st
echo Inflector::ordinalize(2); // outputs 2nd
echo Inflector::ordinalize(3); // outputs 3rd
echo Inflector::ordinalize(4); // outputs 4th
echo Inflector::ordinalize(5); // outputs 5th
echo Inflector::ordinalize(20); // outputs 20th
echo Inflector::ordinalize(21); // outputs 21st
````

