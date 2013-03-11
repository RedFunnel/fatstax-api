Published Database
=======

For the full XML representation of published database requests, [check out the data reference](data_reference.md#published-database).

Get all published databases (for a list)
--------------------------

`GET /api/v1/published_databases.xml` returns all published databases for the current account.

**Response:**

``` xml
<production-client-databases type="array">
  <production-client-databases>
    ...
  </production-client-databases>
</production-client-databases>
```


Get published database
--------

* `GET /api/vi/published_databases/#{id}.xml` returns a single database record, given its integer ID.

**Response:**

``` xml
<production-client-databases>
  ...
</production-client-databases>
```


Create published database
-----------

* `POST /api/vi/published_databases.xml` creates a new database record for the given list.

A new record is created with a status of `processing`.

**Request:**

``` xml
<production-client-databases>
  <!-- No fields are necessary to initiate a request -->

</production-client-databases>
```

**Response:**

Returns HTTP status code 201 Created on success, with the Location header being set to the URL for the new item. (The new item’s integer ID may be extracted from that URL.)

