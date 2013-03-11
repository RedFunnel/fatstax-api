Data Reference
==============

Import
-------

``` xml
<imports type="array">
  <import>
    <action type="integer">1</action>
    <completed-at type="datetime" nil="true"/>
    <created-at type="datetime">2013-03-11T14:49:23-04:00</created-at>
    <created-rows type="integer">0</created-rows>
    <delete-all-data type="boolean">true</delete-all-data>
    <deleted-rows type="integer">0</deleted-rows>
    <id type="integer">1846</id>
    <in-error-state type="boolean">false</in-error-state>
    <last-error nil="true"/>
    <last-row-processed nil="true"/>
    <notify-email nil="true"/>
    <updated-at type="datetime">2013-03-11T14:49:23-04:00</updated-at>
    <updated-rows type="integer">0</updated-rows>
    <errors/>
    <action-name>Update all data</action-name>
    <status>processing</status>
  </import>
</imports>

```

Published Database
-------

``` xml
<production-client-databases type="array">
  <production-client-database>
    <completed-at type="datetime">2013-03-05T08:43:38-05:00</completed-at>
    <created-at type="datetime">2013-03-05T08:43:26-05:00</created-at>
    <id type="integer">1</id>
    <last-error nil="true"/>
    <notify-email nil="true"/>
    <total-rows type="integer">1006</total-rows>

    <updated-at type="datetime">2013-03-05T08:43:38-05:00</updated-at>
    <errors/>
    <status>complete</status>
  </production-client-database>
</production-client-databases>

```

Staged Database
-------

``` xml
<client-databases type="array">
  <client-database>
    <completed-at type="datetime">2013-03-05T08:43:38-05:00</completed-at>
    <created-at type="datetime">2013-03-05T08:43:26-05:00</created-at>
    <id type="integer">1</id>
    <last-error nil="true"/>
    <notify-email nil="true"/>
    <total-rows type="integer">1006</total-rows>

    <updated-at type="datetime">2013-03-05T08:43:38-05:00</updated-at>
    <errors/>
    <status>complete</status>
  </production-client-database>
</client-databases>
```
