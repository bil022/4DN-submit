# 4DN-submit

## Google Apps Script:
  * https://developers.google.com/apps-script/

## Setup:
  * Modify the key pairs to the correct ones.
  * Onetime run: **setup()** in google script in **setup.gs**.

## workflow
  1.  When user open google spreadsheet, the menu is setup automatically through **OnOpen()** function.
  2.  User modify meta data in google spreadsheet.
  3.  Click menu to call Get/Post/Patch functions, data is converted into **JSON** format, and then submit to http server implemented in **PHP**
  4.  Http server filter the meta data according to schemas defined **schemas.json**, and submit the data to **4DN server**.
  5.  Http server receive the message from 4DN server, and send back to google spreadsheet

## TODO:
  * We should use https instead of http protocol for the communication for http server.
  * Support raw data submission using **URL** format.
  * Support bz2 by converting bz2 to gz automatically.
  * Discuss the machanism of how to control which fields to submit, comparing re-submitting all fields.
