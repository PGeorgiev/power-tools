pgeorgiev/power-tools
===================


Quick links: [Installing](#installing) | [Using](#using) | [Contributing](#contributing)

## Installing

Installing this package requires WP-CLI v0.23.0 or greater. Update to the latest stable release with `wp cli update`.

Once you've done so, you can install this package with following command.

```bash
wp package install git@github.com:pgeorgiev/power-tools.git
```

## Using
This package implements the following commands:

### wp pt social
Create social menu.

~~~
wp pt social <menu-name>
~~~

**OPTIONS**

	<menu-name>
		A descriptive name for the menu.

	[--count=<number>]
		How many social icons? Default: 5

	[--porcelain]
		Output just the new menu id.

**EXAMPLES**

~~~
# Create social menu.
$ wp pt social "My Social Menu"
Success: Social menu created successfully.
~~~

### wp pt front
Manage Front Page Settings.

~~~
wp pt front <mode>
~~~

**OPTIONS**

	<mode>
		Front page mode; `page` or `post`.

**EXAMPLES**

~~~
# Set front page display to static page.
$ wp pt front page
Success: Front page displays set to Static Page.

# Set front page display to latest posts.
$ wp pt front post
Success: Front page displays set to Latest Posts.
~~~

### wp pt image
Display Image Info.

~~~
wp pt image info
~~~

**EXAMPLES**

~~~
# List registered image sizes.
$ wp pt image info
+----------------+-------+--------+------+
| id             | wipth | height | crop |
+----------------+-------+--------+------+
| thumbnail      | 150   | 150    | 1    |
| medium         | 300   | 300    |      |
| large          | 1024  | 1024   |      |
| post-thumbnail | 1200  | 9999   |      |
+----------------+-------+--------+------+
~~~

### wp pt widget
Widget tools

~~~
wp pt widget duplicate
~~~

Duplicate given widget instance and place it just after the widget in the sidebar.

**OPTIONS**

	<widget-id>
		Widget ID to duplicate.

**EXAMPLES**

~~~
# Duplicate text widget.
$ wp pt widget duplicate text-2
Success: Widget duplicated to 'text-3'.
~~~

~~~
wp pt widget test
~~~

Add test widgets to every sidebar.

**EXAMPLES**

~~~
# Add test widgets in each sidebar.
$ wp pt widget test
Success: Test widgets added successfully.
~~~

### wp pt wpbeta
Manage Beta Tester Mode. Requires `WordPress Beta Tester` plugin.

~~~
wp pt wpbeta <mode>
~~~

**OPTIONS**

	<mode>
		Beta mode; `bleeding` or `point`.

**EXAMPLES**

~~~
# Set mode to bleeding edge.
$ wp pt wpbeta bleeding
Success: Mode set to 'Bleeding edge nightlies'.

# Set mode to point release.
$ wp pt wpbeta point
Success: Mode set to 'Point release nightlies'.
~~~

## Contributing

Code and ideas are more than welcome.

Please [open an issue](https://github.com/pgeorgiev/power-tools/issues) with questions, feedback, and violent dissent. Pull requests are expected to include test coverage.
