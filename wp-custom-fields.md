## WP CPT & ACF
*WordPress Custom Post Types and Advanced Custom Fields*

The purpose of this talk is to learn how to create WP custom post types and custom fields. We will create a basic plugin for our custom post type, then use ACF to create custom fields and modify the theme file to display the data on the front-end.

#### Class Outline

1. Make a plugin that creates a custom post type for Hackers (Haxiom members).
2. Add custom fields to the Hacker custom post type.
3. Create templates for the single Hacker view and the Hacker Team view to display the Hacker cpt data.

----------------------------

### PART ONE   

#### Discussion

What is a custom post type?

Why would we want to create them inside a plugin rather than inside the theme?   
*To separate the views (theme) from the data (plugin/database).*

#### WordPress Setup 

*Coming Soon!*

#### Create a CPT Plugin
1. Create a file inside plugins directory named “haxiom-cpt.php”
2. Set up plugin file headers.  
  ```
  <?php
  /*
  Plugin Name: Haxiom Custom Post Types
  Description: Custom Post Types for the Haxiom website.
  Author: Haxiom
  Author URI: http://www.hax10m.com
  */
  ```

3. Underneath the file header info, create a new function.
  ```
  function haxiom_cpt () {

  }
  ```
  
4. Inside the function, use the `register_post_type()` function to create new custom post types.
  ```
  register_post_type( 'hacker', array(
  	'labels' => array(
    'name' => 'Hackers',
    'singular_name' => 'Hacker',
   	),
  	'description' => 'Hacker Profile',
  	'public' => true,
  	'menu_position' => 20,
  	'supports' => array( 'title', 'editor', 'thumbnail', 'custom-fields' )
  ));
  ```

5. Tell WP when to call our newly created function by placing `add_action()` just above the function. We will use the `init` hook to call the function after WP has loaded but before headers are sent. 
  ```
  add_action( 'init', 'haxiom_cpt' );
  ```

6. Make sure the file is saved and go to the Plugins area of the WP Admin Menu. Activate your new plugin and watch the custom post type appear in the Admin Menu!

#### Advanced Custom Fields

*Coming Soon!*

----------------------------

### PART TWO  

*Coming Soon!*

----------------------------

### RESOURCES

[Adding Custom Fields to a Custom Post Type, the Right Way](http://blog.teamtreehouse.com/adding-custom-fields-to-a-custom-post-type-the-right-way)   
[WP Codex: Writing a Plugin](http://codex.wordpress.org/Writing_a_Plugin)   
[WP Codex: register_post_type()](http://codex.wordpress.org/Function_Reference/register_post_type)   
[WP Codex: add_action()](http://codex.wordpress.org/Function_Reference/add_action)   
[WP Codex: init](http://codex.wordpress.org/Plugin_API/Action_Reference/init)   
[Advanced Custom Fields](http://www.advancedcustomfields.com/)   

