With the *example* handler you can enable a login prompt for OS.js.

## Setup

```
# Change `handler` to `example`
$ edit src/conf/000-base.json

# Update configuration and template files
$ grunt config dist-index dist-dev-index

# Rebuild (only required if you use `dist`)
# grunt core

```

### Configure

Then set up the configuration in these files (you only need to edit the one you use):

- `src/server/php/handlers/example/handler.php`
- `src/server/node/handlers/example/handler.php`


### Mysql Database table

Create this table:

```
CREATE TABLE IF NOT EXISTS `users` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `username` varchar(255) NOT NULL,
  `password` varchar(255) NOT NULL,
  `name` varchar(255) NOT NULL,
  `groups` text,
  `settings` text,
  PRIMARY KEY (`id`)
) ENGINE=MyISAM  DEFAULT CHARSET=latin1 AUTO_INCREMENT=2 ;
```
