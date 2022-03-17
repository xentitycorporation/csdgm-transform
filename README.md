  npm install

  gem install adiwg-mdtranslator

  echo csdgm_ids.txt | while read name; do npx xslt3 -s:csdgm/$name-csdgm.xml -xsl:/Users/tim/geoplatform/GeoPlatform/infrastructure/lambdas/functions/cache-metadata-from-data-gov/src/fgdcrse2iso19115-2.sef -o:xslt-transformed/$name.iso.xml; done

  cat csdgm_ids.txt | while read name; do mdtranslator translate csdgm/$name-csdgm.xml --reader=fgdc --writer=iso19115_2 > md-translator-transformed/$name.iso.xml; done

## Failed transform through mdTranslator

### 03400647-dc8e-4cc4-b736-0a5aad6de4e9-csdgm.xml
### 1c8a66db-cdc1-48bb-b257-0a90dc5ca912-csdgm.xml
### 4762efd6-433e-4f7a-a85b-afc476058e67-csdgm.xml
### cf453d53-de46-4604-8ff4-db1b89aeffa5-csdgm.xml
### e904dba9-699b-4920-902f-1eac855f4152-csdgm.xml

- not a csdgm file


### 0013a185-38a9-47dd-be86-d8e119545dba-csdgm.xml
### 11d06408-650d-415b-bd7b-0bacefed291b-csdgm.xml
### 332a809d-9c5e-4014-85cb-d444566c10d5-csdgm.xml
### 38fcb6e7-11f4-45d7-a6ce-b4b162ca405d-csdgm.xml
### 672cebcc-af3a-4382-b3c2-66895f85a76b-csdgm.xml
### eca763b9-52b3-4b7e-9fab-34f718446ae1-csdgm.xml

    4: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/adiwg-mdtranslator-2.17.1/lib/adiwg/mdtranslator/writers/iso19115_2/classes/class_temporalExtent.rb:49:in `block (2 levels) in writeXML'
    3: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/adiwg-mdtranslator-2.17.1/lib/adiwg/mdtranslator/writers/iso19115_2/classes/class_timePeriod.rb:41:in `writeXML'
    2: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/builder-3.2.4/lib/builder/xmlbase.rb:69:in `tag!'
    1: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/builder-3.2.4/lib/builder/xmlbase.rb:176:in `_nested_structures'
    /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/adiwg-mdtranslator-2.17.1/lib/adiwg/mdtranslator/writers/iso19115_2/classes/class_timePeriod.rb:54:in `block in writeXML': undefined method `empty?' for nil:NilClass (NoMethodError)


### 061ae6a4-828d-4053-848d-b289d6f17115-csdgm.xml
```xml
<timeinfo>
    <sngdate>
      <caldate>1901-2020</caldate>
```

Failed
Input failed to pass either file structure, validation, or content requirements
See following messages for further information
Success - Input structure is valid
Success - Input content passes schema definition
Fail - Reader execution failed - see following message(s):

Message: 1
ERROR: FGDC reader: Conversion of dateTime string to object failed

Message: 2
WARNING: FGDC reader: identification section time period is missing

Message: 3
WARNING: FGDC reader: BIO geographic description is missing

Message: 4
WARNING: FGDC reader: BIO lineage methodology section is missing


### 0b0b375e-8575-4a21-b0de-5aadcd545ccd-csdgm.xml

```xml
<srccite>
  <citeinfo>
    <origin>USEPA Region 9</origin>
    <pubdate>December, 2006</pubdate>
```
Failed
Input failed to pass either file structure, validation, or content requirements
See following messages for further information
Success - Input structure is valid
Success - Input content passes schema definition
Fail - Reader execution failed - see following message(s):

...

Message: 28
ERROR: FGDC reader: Conversion of dateTime string to object failed


### 43ee676d-04b0-4b49-b485-daaa2103c66c-csdgm.xml

```xml
<timeinfo>
  <sngdate>
    <caldate>2013-2014</caldate>
```

Failed
Input failed to pass either file structure, validation, or content requirements
See following messages for further information
Success - Input structure is valid
Success - Input content passes schema definition
Fail - Reader execution failed - see following message(s):

Message: 1
ERROR: FGDC reader: Conversion of dateTime string to object failed

Message: 2
WARNING: FGDC reader: identification section time period is missing

...


### 44092cbc-9f8c-4ab4-8338-f2a1469692a7-csdgm.xml
### 62a9186b-c25e-481e-9fdf-f2e21c6f38fb-csdgm.xml
### 8cfae25c-565f-4ea0-83e5-b90cda604829-csdgm.xml
### d49b196e-cc0c-4f01-b36a-d1ee4e4b1b47-csdgm.xml
### d55bb218-f3a2-4477-ae86-40d3376a55d7-csdgm.xml
### d8ff99a2-5634-4dcb-b1da-8ec5d79ee14c-csdgm.xml
### e2aa2f25-2f8a-46d3-a213-9867e2542861-csdgm.xml
### e6523c16-d87e-4b7e-b2dc-3ef6f6fe5324-csdgm.xml
### fab711b6-6e25-472c-b642-31a6cec8c920-csdgm.xml

    2: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/nokogiri-1.13.3-x86_64-darwin/lib/nokogiri/xml/node_set.rb:233:in `block in each'
    1: from /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/adiwg-mdtranslator-2.17.1/lib/adiwg/mdtranslator/readers/fgdc/modules/module_horizontalReference.rb:35:in `block in unpack'
    /Users/tim/.rbenv/versions/2.6.4/lib/ruby/gems/2.6.0/gems/adiwg-mdtranslator-2.17.1/lib/adiwg/mdtranslator/readers/fgdc/modules/module_horizontalPlanar.rb:59:in `unpack': undefined method `empty?' for nil:NilClass (NoMethodError)

### 496e9d04-8434-4363-9ceb-0d313ceb0c53-csdgm.xml
### eeacbc70-d696-44a1-b4f8-6cba5789b0c3-csdgm.xml

not sure what it's bailing on - TZ

Failed
Input failed to pass either file structure, validation, or content requirements
See following messages for further information
Success - Input structure is valid
Success - Input content passes schema definition
Fail - Reader execution failed - see following message(s):

...

Message: 3
ERROR: FGDC reader: Conversion of dateTime string to object failed

Message: 4
WARNING: FGDC reader: lineage procedure date is missing

### bdf9fed2-80ed-421f-8325-600a7c7c1c540-csdgm.xml

```xml
<timeinfo>
  <sngdate>
    <caldate>2013-2014</caldate>
```

Failed
Input failed to pass either file structure, validation, or content requirements
See following messages for further information
Success - Input structure is valid
Success - Input content passes schema definition
Fail - Reader execution failed - see following message(s):

Message: 1
ERROR: FGDC reader: Conversion of dateTime string to object failed

...




