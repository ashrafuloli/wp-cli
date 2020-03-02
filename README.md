# WP CLI
- https://wp-cli.org/
- Online handbook
  - https://make.wordpress.org/cli/handbook/
- Online command reference
  - https://developer.wordpress.org/cli/commands/
- https://www.youtube.com/watch?v=cXmMu1sOzEQ&t
- Built-in user manual
  - wp help <command> / wp --help
- Guided interactive mode
  - wp <command> --prompt

## List

* [Cli Comments](https://github.com/ashrafuloli/wp-cli/#cli-comments)
* [Create Config File](https://github.com/ashrafuloli/wp-cli/#create-config-file)
* [WP Database Create](https://github.com/ashrafuloli/wp-cli/#wp-db-create)
* [WP Install](https://github.com/ashrafuloli/wp-cli/#wp-install)
* [Run Server](https://github.com/ashrafuloli/wp-cli/#run-server)
* [WP Theme](https://github.com/ashrafuloli/wp-cli/#wp-theme)
* [WP Plugin](https://github.com/ashrafuloli/wp-cli/#wp-plugin)
* [WP Post](https://github.com/ashrafuloli/wp-cli/#wp-post)
* [WP Scaffold](https://github.com/ashrafuloli/wp-cli/#wp-scaffold)

## Setup Your Environment
- first you copy "bin" folder in your C:\Users\ {Your-Name}
- Widnows Search { environment variables }
- Go to ->  Advanced Tab  ->  Environment Variables ->  Select {Path} ->  Click Edit  -> Add Next 3 Line
- C:\Users\{bin-file-location}
- C:\xampp\php
- C:\xampp\mysql\bin

## Project
Now go to the project file and open command line.
- Make directory `mkdir learn-wp`
- Clear Screen  `cls`

# Cli Comments
- https://developer.wordpress.org/cli/commands/
- `wp core download`

### Create Config File
- https://developer.wordpress.org/cli/commands/config/create/
- `wp config create --dbname=learn_wp --dbuser=root`

### WP DB Create
- https://developer.wordpress.org/cli/commands/db/create/
- `wp db create`

### WP Install
- https://developer.wordpress.org/cli/commands/core/install/
- `wp core install --url="localhost/learn-wp" --title="Learn Wp" --admin_user="rejbioli" --admin_password="123456" --admin_email="rock.ashraful@gmail.com"`

### Run Server
- https://developer.wordpress.org/cli/commands/server/
- `wp server --host=localhost --port=80` or Go to localhost/project-name

### WP Theme
- https://developer.wordpress.org/cli/commands/theme/
- `wp theme list`
- `wp theme activate twentynineteen`
- `wp theme install hello-elementor --activate`
- `wp theme delete twentytwenty`

### WP Plugin
- https://developer.wordpress.org/cli/commands/theme/
- `wp plugin list`
- `wp plugin install elementor`
- `wp plugin activate elementor`
- `wp plugin install contact-form-7 --activate`
- `wp plugin install advanced-custom-fields jetpack ninja-forms --activate`
- `wp plugin install advanced-custom-fields jetpack https://mysite/myplugin.zip --activate`
- `wp plugin delete hello`
- `wp plugin deactivate wordpress-seo`
- `wp plugin deactivate --all`
- `wp plugin update wordpress-seo`

### WP Post
- https://developer.wordpress.org/cli/commands/post/
- https://developer.wordpress.org/cli/commands/post/generate/
- `wp post create --post_type=post --post_title="test post cli" --post_status="publish"` Generate Post
- `wp post delete 12` Delete Post by Id
- `curl -N http://loripsum.net/api/5 | wp post generate --post_content --count=10` Generate Post By Api

### WP Scaffold
- https://developer.wordpress.org/cli/commands/scaffold/
- `wp scaffold plugin sample-plugin` Generate Plugin Init
- `wp scaffold _s sample-theme --theme_name="Sample Theme" --author="Ashraful Oli"` Generate Theme Init by Underscores
- `wp scaffold post-type movie --label=Movie --theme=sample-theme` Generate Post Type


# Site management
> WP-CLI loads before WordPress, allowing control over what loads.
- Reinstall WordPress Core:
  - `wp core download --skip-content --force`
- Skip loading all or some plugins or themes:
  - `--skip-plugins `
  - `--skip-plugins=a-slow-plugin `
  - `--skip-themes `
- Show all PHP errors:
  - `--debug `
- Search And Replace
  - `wp search-replace oldstring newstring`
- Reset user passwords
  - `wp user update rock.ashraful@gmail.com --user_pass=1234567`
- Create a POT
  - `wp i18n make-pot`
  - https://developer.wordpress.org/cli/commands/i18n/make-pot/ 
- Control Maintenance Mode
  - `wp maintenance-mode activate`
  - `wp maintenance-mode deactivate`
  - `wp maintenance-mode status`
- Define
  - https://developer.wordpress.org/cli/commands/config/set/
  - ` wp config set WP_DEBUG true `
  - ` wp config set WP_SITEURL "http://localhost/wedevs-academy" `
  - ` wp config set WP_HOME "http://localhost/wedevs-academy" `
  
  



  
