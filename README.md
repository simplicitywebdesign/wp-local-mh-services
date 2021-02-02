# wp-local-mh-services

A WordPress plugin to display local mental health services information.

This plugin adds (through shortcodes, php template tags and/or widgets) a front-end interface whereby visitors to a site can see/access information regarding their local mental health support services in their region. Particularly useful for appending to articles discussing difficult topics such as suicide, sexual assault, domestic violence, etc.

If access to location is provided by the user, they will see their local service, if not provided, a dropdown allowing them to filter a master list. 

## Proposed usage

### Shortcode

~~~text
[local-mh-services
	use_geolocation="true|false"
	show_links="true|false"
	show_active_services="true|false"
	show_local_notice="true|false"
] Content to display as the notice at the end of the article [/local-mh-services]
~~~

### PHP Template tag

~~~php
<?
	local_mh_services($settings = array(
		'use_geolocation' => true,
		'links' => true,
		'display_active' => true,
		'local_notice' => $string
	));
?>
~~~

## Changelog

v0.1.01: 2 February 2021
:Add organisational data schemas for JSON datasets: services, country info and codes.
:`data/countries.json` features country information[^1].
:`data/services.json` will eventually contain service information, at present it is serving primarily as an in-progress schema layout whilst data field requirements are assessed.[^2]

v0.1.00: 2 February 2021
:Set up the initial framework and establish plugin structure

## Sources
[^1]: Country data [https://datahub.io/core/country-codes] Last updated 02 February 2021
[^2]: Services gleaned from Wikipedia [https://en.wikipedia.org/wiki/List_of_suicide_crisis_lines] Last updated 02 February 2021