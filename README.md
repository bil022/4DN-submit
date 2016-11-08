# 4DN-submit

## workflow
  1.  User edit in google spreadsheet
  2.  User click menu to evoke functions written in *google script*. The scripts convert the fields into *JSON* format, and submit to local http server (*centos*)
  3. Local http server check the JSON objects with *schemas.json*, and filter out the fields that need to be submit to *4DN server*.
  4. Local http server receive the message from 4DN server, and send back to google spreadsheet

## google script setup
  1. The key is scored locally using 

## TODO:
  https
  Support http file
  conver bz2 to gz
  patch
