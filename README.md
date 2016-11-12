CMB2 Icon Picker
==================

A [CMB2](https://github.com/WebDevStudios/CMB2) custom field that let you pick icons to use in posts etc.. 
This icon picker is using [dashicons](https://developer.wordpress.org/resource/dashicons/) by default, but it is super easy to add and use your own icon fonts.

Features:

* Add your own custom icon fonts.
* Works with repeatable groups.
* Works as radio and multicheck.


## Example

```php
// Classic CMB2 declaration
$cmb = new_cmb2_box( array(
	'id'           => 'prefix-metabox-id',
	'title'        => __( 'Post Info' ),
	'object_types' => array( 'post', ), // Post type
) );

// Add new field
$cmb->add_field( array(
	'name'        => __( 'Post icon' ),
	'id'          => 'prefix_post_icon',
	'desc'          => __( 'Of course description is supported.' ),
  'show_names' => true,			
	'type'    => 'icon_picker',
	'options' => array(
		// Select icons we want to show (shows all dashicons by default).
		'icons' => array('dashicons-menu','dashicons-dashboard','dashicons-admin-site'),
		// Use as multicheck instead of radio, deafult is false. 
		'multicheck' => true,
	),	
) );
```

Note that by default this field will output selected icon class as string, but will output as array if multicheck is used. 

## Using your own icon font.

## Screenshots

1. Field display
![Field display](https://raw.githubusercontent.com/lassemt/cmb2-icon-picker/master/icon-picker-field.png)`