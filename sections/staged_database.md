Staged Database
=======

For the full XML representation of stage database requests, [check out the data reference](data_reference.md#staged-database).

Get all staged databases (for a list)
--------------------------

`GET /api/v1/staged_databases.xml` returns all staged databases for the current account.

**Response:**

``` xml
<client-databases type="array">
  <client-databases>
    ...
  </client-databases>
</client-databases>
```


Get staged database
--------

* `GET /api/vi/staged_databases/#{id}.xml` returns a single database record, given its integer ID.

**Response:**

``` xml
<client-databases>
  ...
</client-databases>
```


Create staged database
-----------

* `POST /api/vi/staged_databases.xml` creates a new database record for the given list.

A new record is created with a status of `processing`.

**Request:**

``` xml
<client-databases>
  <!-- No fields are necessary to initiate a request -->
  
</client-databases>
```

**Response:**

Returns HTTP status code 201 Created on success, with the Location header being set to the URL for the new item. (The new item’s integer ID may be extracted from that URL.)

