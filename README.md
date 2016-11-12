# Content menu

> Work in progress

Adds a content menu to WordPress admin where all your post types that are used for content can live, when doing this the post type configured to use content menu will be removed from the admin menu and if you have a lot of post types you will see a more clean admin menu than before.

## Installation

```sh
composer require frozzare/wp-content-menu
```

## Usage

To move your post types into content menu you can set `content_menu` to `true` in `register_post_type` or use a filter.

```php
// With `register_post_type`
register_post_type( 'book', [
  'content_menu' => true
] );

// With the filter.
add_filter( 'content_menu_post_types', function () {
  return ['page', 'post', 'book']
} );
```

## Screenshots

![](https://cloud.githubusercontent.com/assets/14610/20240391/4ab1f8d0-a917-11e6-9994-616924b94f53.png)

![](https://cloud.githubusercontent.com/assets/14610/20239328/5ee39264-a8fe-11e6-940b-77658b2f0b0b.png)

## Contributing

Everyone is welcome to contribute with patches, bug-fixes and new features.

## License

MIT © [Fredrik Forsmo](https://github.com/frozzare)
