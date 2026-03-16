# The Vessel Database
This is a SQLite3 database of container ships and their lashing gear. It is free to use and updated roughly weekly. Most of this data started with Rey from ILWU Local 13 and is now maintained by [Blake](mailto:feedback@besz.ca) from ILWU Local 514.

You can access an searchable interface to the database at [lashing.ca](https://lashing.ca/).

## Terminology
I have tried to use the [MacGregor product catalogue](https://www.macgregor.com/globalassets/picturepark/imported-assets/65120.pdf) terms or the terms the crew use for field names. Here is a quick reference:

- "External" lashing is "Knuckle" or "Chinese"
- "Horizontal" lashing is "Belly" or "Barrel" or "Torpedoes"
- "Twistlocks" are the above deck "Cones" or "Stackers"
- "Midlocks" are "Bananas" or the cones between tight 20's on deck
- "Guts" is the lashing between 20's on deck
- "Decklocks" are "Deck Stackers" and are used to secure the containers to the lid
- "Lashing Bridges" are "Catwalks" or "Walkways"

## Linking
If you already have an online despatch system, you can pass the vessel name like so:

`https://ilwu.besz.ca/vessels/?name=VESSEL+NAME` -- just be sure to convert all spaces to plus '+' signs.

## Compiling
To build the database, you can run the SQLite3 command:

```sqlite3 vessels.db < vessels.sql```

## Release Schedule
Aside from individual vessel updates, an automated task runs every Saturday morning (Pacific Time) to update all the vessel names based on their IMO. If you are using this database on your own website, downloading the latest release every Saturday night will ensure you have the latest data.

## Downloading The Latest Release
You can automatically download the latest release by running:

```curl -LO https://github.com/vesseldatabase/vesseldatabase/releases/latest/download/vessels.db```

## License
This database is [licensed by a Creative Commons BY-NC-SA license](https://github.com/vesseldatabase/vesseldatabase?tab=License-1-ov-file). Basically, you must link to either this repository or [https://ilwu.besz.ca/vessels](https://ilwu.besz.ca/vessels/) and you cannot use this database for commercial use. If you are running a paid website or application, this database must be part of a free portion of that site or application. In addition, any derivative work must include this same license.
