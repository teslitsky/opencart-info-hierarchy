OpenCart Info Hierarchy
=======================

OpenCart vQmod plugin that adds a hierarchy of information pages and the ability to control their output in the header and footer

How to install
--------------
* make sure you have installed vQmod
* copy ```vqmod_information_pages_hierarchy.xml``` file to ```vqmod/xml``` folder
* run following SQL, that adds fields to your DB. If you don't use prefixes - remove ```oc_``` in this SQL

```SQL
ALTER TABLE `oc_information`
ADD COLUMN `oc_parent_id` INT(10) NULL DEFAULT NULL AFTER `status`,
ADD COLUMN `oc_position_header` TINYINT(1) NOT NULL DEFAULT '0' AFTER `parent_id`;
```
License
-------
MIT: http://rem.mit-license.org
