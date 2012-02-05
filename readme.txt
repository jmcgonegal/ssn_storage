
The ssn storage module allows per field storage of validated unique social 
security and tax id numbers.

Features:
 - Unique ssn
 - Basic ssn validation
 - Hashed ssn
 - Last 4 digits stored seperately for display


Use
---
Replace 'your_content_type' in examples below with the machine name of your 
content

Add the field 'Social Security Number' to your_content_type
/admin/structure/types/manage/your_content_type/fields

Select how you want your field to look: 
/admin/structure/types/manage/your_content_type/display
 - Last 4 digits (####) 
 - Last 4 digits with hidden (***-**-####)
 

Security
--------
The full social security number is hashed based on the salt in the settings.php 
for drupal. If an attacker gets php eval permission or your settings.php file 
is stolen along with your database it would be fairly trivial to expose hashed 
social security numbers.


Author
------
John McGonegal
john@plainfast.com
