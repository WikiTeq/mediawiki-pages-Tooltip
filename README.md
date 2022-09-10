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

# Usage examples

The template has the following unnamed parameters:

* 1 - the text to display inside a tooltip (required)
* 2 - tooltip icon type `info`, `warning`, `error`, `note`
* 3 - max. width of the tooltip window in pixels without prefix, eg: `100`
* 4 - theme, can be empty for default (with rounded corners) or `square-border`, `square-border-light`

```
{{Tooltip|This is a tooltip text}}
{{Tooltip|This is a tooltip text|warning}}
{{Tooltip|This is a tooltip text|info|300}}
{{Tooltip|This is a tooltip text|error|300|square-border-light}}
```

Navigate to `Template:Tooltip` for more detailed usage examples
