# WP CLI
- https://developer.wordpress.org/cli/commands/
- https://www.youtube.com/watch?v=cXmMu1sOzEQ&t
- [Cli Comments](https://github.com/ashrafuloli/wp-cli/blob/master/README.md#cli-comments)

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
- `wp plugin delete hello`

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
