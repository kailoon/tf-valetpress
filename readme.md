### ValetPress for ThemeForest Review Team

To create WordPress site locally quickly with [Valet](https://laravel.com/docs/8.x/valet) and install a few plugins to get started with.

## Plugins

- [envato theme check](https://github.com/envato/envato-theme-check)
- [block unit test](https://wordpress.org/plugins/block-unit-test/)
- [debug bar](https://wordpress.org/plugins/debug-bar/)
- [woocommerce](https://wordpress.org/plugins/woocommerce/)
- [envato elements](https://wordpress.org/plugins/envato-elements/)
- [elementor](https://wordpress.org/plugins/elementor/)
- [Monster Widget](https://wordpress.org/plugins/monster-widget/)

This is a slight modified version from [AaronRutley's version](https://github.com/AaronRutley/valetpress).

## Installation

1. Install [Valet](https://laravel.com/docs/8.x/valet)
2. Install [WP-CLI](https://wp-cli.org/)
3. Download / Clone this repo into a directory like `~/.valetpress`
4. Edit the valetpress file as you need.
5. Include the valetpress script in your `.bashrc` or `.zshrc` or similar file.

```
if [ -f ~/.valetpress/valetpress ]; then
    source ~/.valetpress/valetpress
else
    print "404: ~/.valetpress/valetpress not found."
fi
```

## Available Commands & What It Does

`vp create`

- Will ask for the name of your project, enter something like `myproject`.
- Download WordPress into a directory like `~/Sites/myproject`
- Setup the mysql database called `myproject`
- Create `wp-config.php` file & set `'WP_DEBUG' = TRUE`, `'WP_MEMORY_LIMIT' = 512M`.
- Delete plugins `hello`, `akismet`.
- Delete themes `twentynineteen`, `twentytwenty`.
- Install plugins.
- Import demo content from https://raw.githubusercontent.com/WPTT/theme-unit-test/master/themeunittestdata.wordpress.xml
- Access admin via `http://myproject.test/wp-admin/` with username as `myproject` and password as `password`.

`vp empty`

Same as `create` but without demo content.
