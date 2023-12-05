# Open Refine Template John L. Wallace Korean War Training Photo Album


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["Identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo supplied="yes"><title>' + cells["title"].value + '</title></titleInfo>')}} 

{{if(isBlank(cells['abstract'].value), '', '<abstract>' + cells["abstract"].value + '</abstract>')}}

<originInfo>
{{if(isBlank(cells['date_created'].value), '', '<dateCreated>' + cells['date_created'].value + '</dateCreated><dateCreated encoding="edtf">' + cells['date_created_edtf'].value + '</dateCreated>')}}
{{if(isBlank(cells['date_created_approx'].value), '', '<dateCreated qualifier="approximate">' + cells['date_created_approx'].value + '</dateCreated><dateCreated encoding="edtf" qualifier="approximate" point="start">' + cells['date_approx_start'].value + '</dateCreated><dateCreated encoding="edtf" qualifier="approximate" point="end">' + cells['date_approx_end'].value + '</dateCreated>')}}
{{if(isBlank(cells['publisher'].value), '', '<publisher>' + cells['publisher'].value + '</publisher>')}}
{{if(isBlank(cells['place_origin'].value), '', '<place><placeTerm valueURI="' + cells['place_origin_URI'].value + '">' + cells['place_origin'].value + '</placeTerm></place>')}}
</originInfo>

{{if(isBlank(cells['Creator'].value), '', '<name><namePart>' + cells['Creator'].value + '</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>')}}

<physicalDescription>
{{if(isBlank(cells['form'].value), '', '<form authority="aat" valueURI="' + cells['form_URI'].value + '">' + cells['form'].value + '</form>')}}
{{if(isBlank(cells['form2'].value), '', '<form authority="aat" valueURI="' + cells['form2_URI'].value + '">' + cells['form2'].value + '</form>')}}
{{if(isBlank(cells['Extent'].value), '', '<extent>' + cells["Extent"].value + '</extent>')}}
</physicalDescription>

{{if(isBlank(cells['subject'].value), '', '<subject valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo'].value), '', '<subject authority="naf" valueURI="' + cells['subject_geo_URI'].value + '"><name><namePart>' + cells['subject_geo'].value + '</namePart></name></subject>')}}

{{if(isBlank(cells['Note2'].value), '', '<note>' + cells['Note2'].value + '</note>')}}

<typeOfResource>{{cells['typeOfResource'].value}}</typeOfResource>
{{if(isBlank(cells['typeOfResource2'].value), '', '<typeOfResource>' + cells['typeOfResource2'].value + '</typeOfResource>')}}

{{if(isBlank(cells['language'].value), '', '<language><languageTerm type="text" authority="iso639-2b">' + cells['language'].value + '</languageTerm></language>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>John L. Wallace Korean War Training Photo Album</title></titleInfo></relatedItem>

<relatedItem displayLabel="Collection" type="host">
<titleInfo>
<title>John L. Wallace Korean Conflict Photo Album</title>
</titleInfo>
<identifier>MS-3989</identifier>
</relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```