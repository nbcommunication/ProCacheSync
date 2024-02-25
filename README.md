# ProCache Sync
Synchronises ProCache clearing across a multi-instance environment.

## Overview
The main purpose of this module is to allow ProCache to be used in an auto-scaling multi-instance environment.

# How it works
When a page is saved and cache clearing is triggered, the data (methods / arguments) associated with that clear are saved to the database. ProCacheSync runs a check every 30 seconds to look for records in the database since ProCache was last cleared. If it finds any it processes them as ProCache would. Any records it finds will have been generated by a clear on another server instance, thus enabling multiple instances of ProCache to stay approximately synchronous.

## Installation
1. Download the [zip file](https://github.com/nbcommunication/ProCacheSync/archive/master.zip) at Github or clone the repo into your `site/modules` directory.
2. If you downloaded the zip file, extract it in your `sites/modules` directory.
3. In your admin, go to Modules > Refresh, then Modules > New, then click on the Install button for this module.

**ProcessWire >= 3.0.210 and PHP >= 8.1.0 are required to use this module.**

## License
This project is licensed under the Mozilla Public License Version 2.0.
