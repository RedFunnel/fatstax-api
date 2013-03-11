Import
=======

For the full XML representation of import requests, [check out the data reference](data_reference.md#import).

Get all imports (for a list)
--------------------------

`GET /api/v1/imports.xml` returns all imports for the current account.

**Response:**

``` xml
<imports type="array">
  <import>
    ...
  </import>
</imports>
```


Get import
--------

* `GET /api/vi/imports/#{id}.xml` returns a single import record, given its integer ID.

**Response:**

``` xml
<import>
  ...
</import>
```


Create import
-----------

* `POST /api/vi/imports.xml` creates a new import record for the given list.

A new record is created with a status of `processing`.


**Request:**

``` xml
<import>
  <!-- There are two possbile actions: 'Update all data' => 1, 'Only update pricing for existing SKUs' => 2 --> 
  <action type="integer">1</action>
  <!-- Should we wipe the catalog before attempting the import? -->
  <delete-all-data type="boolean">true</delete-all-data>
  <!-- The file name on the FTP server for your account. -->
  <ftp-file-name>testfile2.csv</ftp-file-name>
  <!-- You can optionally send a status update to one or more email addresses (up to 25) separated by commas and/or semi-colons. -->
  <notify-email nil="true"/>
  <!-- -->
</import>
```

**Response:**

Returns HTTP status code 201 Created on success, with the Location header being set to the URL for the new item. (The new item’s integer ID may be extractd from that URL.)


Destroy item
------------

* `DELETE /api/v1/imports/#{id}.xml` destroys the given import record.

**Response:**

Returns HTTP status code 204 on success.
