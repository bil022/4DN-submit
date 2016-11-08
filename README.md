# 4DN-submit

## google script one-time setup
  * Run google script: **PropertiesService.getUserProperties().setProperty("4DN-server", "key:pairs");** in **init.gs**

## workflow
  1.  User open google spreadsheet, the menu is setup through **OnOpen()** function.
  2.  User edit meta data using google spreadsheet.
  3.  User click menu to call Get/Post/Patch functions, data is converted into **JSON** format, and submit to local http server written in **PHP**
  4.  Local http server match the fields of JSON objects defined in **schemas.json**, and submit the fields that defined for **4DN server**.
  5.  Local http server receive the message from 4DN server, and send back to google spreadsheet

## TODO:
  https
  Support http file
  conver bz2 to gz
  patch
