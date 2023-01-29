# Instructions - QB-Core
Support Discord: https://discord.gg/PkJGQ6EdZp
## 1. Items
Add the items!
### 1a. items.lua
```lua
	-- qb-houserobbery by PenguScripts
	['mask'] 			 			 = {['name'] = 'mask', 							['label'] = 'Stone Mask', 				['weight'] = 5000, 		['type'] = 'item', 		['image'] = 'mask.png', 				['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Expensive looking stone mask'},
	['painting'] 					 = {['name'] = 'painting', 						['label'] = 'Painting', 				['weight'] = 15000, 	['type'] = 'item', 		['image'] = 'painting.png', 			['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Expensive looking painting'},
	['bowl'] 						 = {['name'] = 'bowl', 							['label'] = 'Bowl', 					['weight'] = 1000, 		['type'] = 'item', 		['image'] = 'bowl.png', 				['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'A bowl.'},
	['printeddetails'] 				 = {['name'] = 'printeddetails', 				['label'] = 'Printed Details', 			['weight'] = 100, 		['type'] = 'item', 		['image'] = 'printeddetails.png', 		['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'This is a code. Into what though?'},
	['alarmclock'] 					 = {['name'] = 'alarmclock', 					['label'] = 'Alarm Clock', 				['weight'] = 2000, 		['type'] = 'item', 		['image'] = 'alarmclock.png', 			['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'Beep Beep.'},
	['book'] 						 = {['name'] = 'book', 							['label'] = 'Book', 					['weight'] = 750, 		['type'] = 'item', 		['image'] = 'book.png', 				['unique'] = true, 		['useable'] = false, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'This is for you Bookworm!'},
	['bong'] 						 = {['name'] = 'bong', 							['label'] = 'Bong', 					['weight'] = 1500, 		['type'] = 'item', 		['image'] = 'bong.png', 				['unique'] = true, 		['useable'] = true, 	['shouldClose'] = true,	   ['combinable'] = nil,   ['description'] = 'I choose green team!'},
	-- IF YOU HAVE A BONG, DO NOT ADD THE BONG FILES!

```
### 1b. Images
Get the images from pn-houserobbery -> images, then move them to qb-inventory -> html -> images
## 2. Optional Dependencies!
Check the config for the links corresponding to the Dependencies!

## 3. Configure The Script!
Loads of more configurable options are arriving in the near future, so prepare yourselves!

# Instructions - ESX

## 1. Items
Add items using the SQL file provided, removing any lines for items that are already included on your server. Each items weight should also be configured according to your servers standards. 
### 1a. pn-houserobbery.sql
```sql

-- USE FOR ESX. If any of the items already exist in your server, remove the line of SQL code pertaining to that item. --

INSERT INTO `items` (`name`, `label`, `weight`) VALUES
	('painting', 'Painting', 1),
    ('printeddetails', 'Printed Details', 0.1),
    ('alarmclock', 'Alarm Clock ', 1),
    ('bowl', 'Bowl', 1),
    ('lockpick', 'Lockpick', 1),
    ('pistol_ammo', 'Pistol Ammo', 1),
    ('smg_ammo', 'SMG Ammo', 1),
    ('rifle_ammo', 'Rifle Ammo', 1),
    ('BONG ITEM NAME HERE', 'BONG LABEL HERE', 1),
    ('armor', 'armor', 1),
    ('phone', 'Phone', 1),
    ('book', 'Book', 1),
    ('goldbar', 'Gold Bar', 1),
    ('10kgoldchain', '10k Gold Chain', 1),
    ('rolex', 'Rolex', 1),
    ('mask', 'Mask', 1)
    
;
```
### 1b. Images
If the inventory script that you use requires images, use the ones provided for the qb-core side of the script. Several of the items that do not have provided pictures are default qb-core assets.

## 2. Dependencies
The ESX portion of this script uses https://github.com/wowpanda/progressbar as one dependency for progressbars, and https://github.com/utkuali/Finger-Print-Hacking-Game for the hacking portion. If you have a preferred script to use for the progressbar, that can be configured if you have the open-source version. 

## 3. Configure the Script
For ESX, ensure that `Config.Framework = ESX`. This makes the script run the correct portions for your framework. If you have the open-source version of the script, then you can set `Config.ProgBar` to `OTHER` to set your own progress bar code in the script. 

`Config.ESX_PropertyCompatibility` is important if you plan on using the default esx_property, as it moves the enter/exit locations to allow the home that the robbery is located at to be used as a player home. If you do not use esx_property, you can disable this option. 

For ESX, there is a large portion of configurable options available to change the floating markers that appear at each location. These allow you to change the color, size, bob, and opacity of each marker. More information is available in the `config.lua`, and each configuration option has a comment that explains what each does with what values it can take. 