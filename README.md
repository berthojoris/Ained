# AINED

Theme library for Codeigniter

---

## Features

- All themes and assets in one place
- CSS minify
- LESS minify
- Javascript minify
- Cache control

## Third Party Libraries

- [LessPHP](http://leafo.net/lessphp)
- [JSMIN](https://github.com/rgrove/jsmin-php)

## Installing

- Copy all files and sub-folders from `application` to your application folder,
- Copy the `themes` folder to the root of your Codeigniter path.

The structure :

    /application
        /config
            /theme.php
        /libraries
            /Theme.php
        /third_party
            /Theme
    /system
    /themes
        /default
            /cache
            /css
            /img
            /js
            /index.php

## Setup

	/*
	|--------------------------------------------------------------------------
	| Theme configuration
	|--------------------------------------------------------------------------
	*/
	$config['theme']['path']    	= 'themes';
	$config['theme']['theme']    	= 'default';
	$config['theme']['layout']    	= 'index';
	
	/*
	|--------------------------------------------------------------------------
	| Assets configuration
	|--------------------------------------------------------------------------
	*/
	$config['theme']['css']    		= 'css';
	$config['theme']['js']    		= 'js';
	$config['theme']['img']    		= 'img';
	$config['theme']['cache']    	= 'cache';

## Documentation

	// Autoload
	$autoload['libraries'] = array('theme');


	// Controller
	$this->theme

		 // Set Theme
		 ->set_theme('my_theme')

		 // Set Layout
		 // my_theme/single.php
		 ->set_layout('single')
		
		 // Block
		 // views/my_twitter.php or
 		 // my_theme/blocks/my_twitter.php
		 ->block('twitter', 'user/test')

		 // Data
		 ->set('title', 'My first theme')
		 ->set('key', 'value')

		 // View
		 // views/user.php
		 ->view('user');


	// View
	echo $twitter; // Load block
	echo $title;   // Load data










