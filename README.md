# mediawiki-pages-Tooltip
Adds a `Tooltip` template to be used as a wrapper around SMW `#info` [parser function](https://www.semantic-mediawiki.org/wiki/Help:Adding_tooltips)

# Requirements
* [SemanticMediaWiki](https://www.semantic-mediawiki.org/wiki/Semantic_MediaWiki)
* [PageExchange](https://www.mediawiki.org/wiki/Extension:Page_Exchange) or [PagePort](https://gerrit.wikimedia.org/r/admin/repos/mediawiki%2Fextensions%2FPagePort)

# Setup

## via PagePort
* Download the repository
* Run
```php
php extensions/PagePort/maintenance/importPages.php --source ~/mediawiki-pages-Tooltip
```

## via PageExchange
* Add the following line to your LocalSettings.php:
```php
$wgPageExchangePackageFiles[] = 'https://raw.githubusercontent.com/WikiTeq/mediawiki-pages-Tooltip/master/page-exchange.json';
```
* Navigate to Special:Packages and install the package

# Usage
Navigate to `Template:Tooltip` and see the usage examples

