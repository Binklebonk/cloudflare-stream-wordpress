# Cloudflare Stream for WordPress

A fork from the official Cloudflare Stream plugin 1.0.5 for WordPress.

The Gutenberg Block method of adding videos appears to be broken (in the original plugin also) and I plan to remove this feature completely from future versions until resolved.

USE THE SHORTCODE METHOD INSTEAD.  See Shortcode section below.


The original official plugin:
https://wordpress.org/plugins/cloudflare-stream/

Official plugin GitHub page:
https://github.com/cloudflare/stream-wordpress


Changes
------------
* Shortcode method always uses signed URL's / tokens.
* Removed analytics.
* Added additional shortcode options, controls, autoplay, loop, preload and muted.
* Uses API Token based API access, for MUCH more secure Cloudflare account access.
* Uses zones API for more secure Cloudflare account access.
* Any existing API Key, API account email and API account ID stored in the database are deleted when the settins page is accessed.
* If updating from version older than 1.0.6, you'll need to enter your API Token and API Zone ID in the configuration page.
* Add setting for signed URL/token duration (default is currently 1 hour).


To-Do
------------
* Remove broken Gutenberg block.
* Rebuild Gutenberg block with dynamic support for signed URL's.


Issues
------------
* The Gutenberg Block method of adding videos is failing. This is failing in the original plugin too. Shortcode method is working though. Details on how to use it are below.



Installation
------------
* Copy the contents of this repository (excluding the .git folder) to the following location within your WordPress installation:
```
/wp-content/plugins/cloudflare-stream/
```
* In the WordPress admin panel, visit the Plugins section Activate the Cloudflare Stream plugin.


Shortcode
------------

`[cloudflare_stream uid="`_some video id_`"]`

Replace _some video id_ with an actual Cloudflare Stream video ID.

These are optional shortcode flags (with defaults shown here). These are all "true" or "false" options:

* controls="true"
* autoplay="false"
* loop="false"
* preload="false"
* muted="false"


They can be used in this way:

`[cloudflare_stream uid="`_some video id_`" controls="true" autoplay="false" loop="false" preload="false" muted="false"]`


Acknowledgements
----------------
* Cloudflare and WP Engine for developing the original plugin this was forked from.


License
-------

Copyright (C) 2020 Cloudflare

This program is free software; you can redistribute it and/or
modify it under the terms of the GNU General Public License
as published by the Free Software Foundation; either version 2
of the License, or (at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program; if not, write to the Free Software
Foundation, Inc., 51 Franklin Street, Fifth Floor, Boston, MA  02110-1301, USA.

https://www.gnu.org/licenses/old-licenses/gpl-2.0.html
