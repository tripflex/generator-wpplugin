generator-wpplugin [![Build Status](https://secure.travis-ci.org/WebDevStudios/generator-wpplugin.png?branch=master)](https://travis-ci.org/WebDevStudios/generator-wpplugin)
=============================================================================================================================================================================

> [Yeoman](http://yeoman.io) generator for WordPress plugins, based off the [WebDevStudios plugin generator](https://github.com/webdevstudios/generator-wpplugin)

Getting Started
---------------

Pre-requisites: You'll need [node](https://nodejs.org/download/) which comes with [npm](https://github.com/npm/npm#super-easy-install).

If you don't have [Yeoman](http://yeoman.io/) installed:

```bash
npm install -g yo
```

To install generator-wpplugin from npm, run:

```bash
npm install -g generator-wpplugin
```

To use generator-wpplugin, `cd` to your WordPress plugins folder and:

```bash
yo wpplugin
```

You'll be prompted with steps for creating your plugin.

Sub-generators
--------------

Once your nifty new plugin has been generated, `cd` into your new plugin's directory. While in the plugin directory, you can run additional commands called sub-generators to automatically generate files to enhance your plugin.

-	`yo wpplugin:include include-name` [Basic Include](include/README.md)
-	`yo wpplugin:cpt cpt-name` [Custom Post Type](cpt/README.md)
-	`yo wpplugin:options options-name` [Option Page](options/README.md)
-	`yo wpplugin:widget widget-name` [Widget](widget/README.md)
-	`yo wpplugin:js` [Javascript](js/README.md)
-	`yo wpplugin:css` [Styles](css/README.md)

For the names of the include, cpt, options, and widget subgenerators remember that the plugin prefix will be added to the class name so no need to include the original plugin name there! Think of it as the file name for each instead.

Tests
-----

By default the plugin generator adds some built in tests for you to add on to as you develop your plugin! To run these tests run the `install-wp-tests.sh` script in the bin folder with the proper database details for your local setup.

Once you've run the `install-wp-tests.sh` script you can run just `phpunit` in the main folder of your plugin.

If you don't want tests included in your plugin when it is generated run the main generator with the `--notests` option.

### Adding Packages with Composer

If you chose composer as the autoloader option during the plugin's initiation, you can use composer to add additional dependencies.

Let's `cd` into our new plugin's directory and add [CMB2](https://github.com/WebDevStudios/CMB2):

```bash
composer require webdevstudios/cmb2
```

CMB2 will now appear under `vendor`

```bash
-plugins
  -wds-foo-plugin
    -vendor
      -webdevstudios
        -cmb2
```

See the complete list of WebDevStudios packages: https://packagist.org/packages/webdevstudios/
