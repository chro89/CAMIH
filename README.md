# CAMIH - Complementary and Alternative Medicine Insights Hub

This repository is part of the publication "CAMIH - Complementary and Alternative Medicine Insights Hub", which is currently under review at AIME 2025.

It contains the following information:

- All_properties.png is a visualization of the ontology we used to represent evidence in CAMIH.
- properties_and_values.txt contains all properties and their allowed values in our database. If a property does not have an allowed value, users can enter any alphanumeric information.
- Templates: this directory contains all semantic templates ([Link](https://www.semantic-mediawiki.org/wiki/Help:Semantic_templates)) we created to represent information in CAMIH.
- Forms: this directory contains all input forms ([Link](https://www.mediawiki.org/wiki/Extension:Page_Forms)) we created that help users create content in CAMIH.

## Setup instructions
- install SMW according to https://www.semantic-mediawiki.org/wiki/Help:Installation/Quick_guide
- add the following to the bottom of the LocalSettings.php

```
wfLoadExtension( 'PageForms' );
wfLoadExtension( 'SemanticMediaWiki' );
enableSemantics( 'http://your-domain.org', true );
$smwgParserFeatures = $smwgParserFeatures | SMW_PARSER_LINV;
$smwgEnabledFulltextSearch = true;
$wgAllowDisplayTitle = true;
$wgRestrictDisplayTitle = false;
$smwgFulltextSearchMinTokenSize = 1;
```

- create properties, templates, and forms according to the examples given in this repository and adjust to your liking


If you have any questions, let us know!
