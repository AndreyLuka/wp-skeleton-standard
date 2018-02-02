# WordPress Skeleton Standard

WordPress skeleton with Composer, readiness for VCS and standard project structure.  

## Requirements

* [PHP](https://php.net/) >= 5.6
* [Composer](https://getcomposer.org/)
* [WP-CLI](https://wp-cli.org/)

## Installation

1. Go to a new project directory and type:  
`git clone https://github.com/AndreyLuka/wp-skeleton-standard.git .`
2. Copy `wp-config.dist.php` to `wp-config.php` and edit variables (database connection, etc).
3. Choose WordPress version to install: open `composer.json` and find `wp-core-download` script. Edit `--version` parametr. Then run:  
`composer run-script wp-core-download`
4. Run `composer install`
5. Visit site URL to run WordPress installation.
6. Add theme(s)/plugin(s) (read below).

## Themes installation

Install themes using Composer:  
`composer require wpackagist-theme/<theme-name>`

By default, all themes are ignored by git. If you need to keep theme in repository (custom theme, child theme, etc) add this line to .gitignore:  
`!/wp-content/themes/<theme-name>/`

## Plugins installation

Install plugins using Composer:  
`composer require wpackagist-plugin/<plugin-name>`

By default, all plugins are ignored by git. If you need to keep plugin in repository (custom plugin, etc) add this line to .gitignore:  
`!/wp-content/plugins/<plugin-name>/`
