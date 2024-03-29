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

## Markup supported

* Wiki markup (including internal and external links)
* Simple html (including `class` attribute)

# Hints

## Adding a tooltip using the visual editor 

To add a tooltip to a page using the visual editor do the following.

1. Insert the template
* Click the "Insert" menu on the editor toolbar.
* Find the "Template" menu item and click it.

![VE  Insert template menu](https://user-images.githubusercontent.com/62721134/236925043-a3decf93-b496-46b8-81ee-75851dc1d47b.png)

2. Bring up the tooltip dialog
* Type "Tooltip" in the template input.
* Wait for the dropdown item to appear and click it. Click "Add template".

![VE  Insert Tooltip template](https://user-images.githubusercontent.com/62721134/236925042-717271dc-6b0c-4fce-8009-763e6be3cf21.png)

3. Fill out the Tooltip fields
* In the parameter input, type the tooltip text.
* (optional) Add a tooltip type, max width and theme parameters
* Click "Insert".

![VE  Fill out Tooltup template fields](https://user-images.githubusercontent.com/62721134/236925038-6c2ffba7-1299-440d-98e7-1e66a06fe86f.png)

## Special characters in Tooltips 
Some special characters, notably the equals sign (<nowiki>=</nowiki>) can be incorrectly interpreted as HTML as discussed [[smw:Help:Special_characters_in_tooltips|here]]. To avoid this, use the string of characters <code>&amp;#61;</code> instead of the equals sign.


Navigate to `Template:Tooltip` for more detailed usage examples
