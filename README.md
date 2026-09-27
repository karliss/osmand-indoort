# osmand-indoort
Experimental OsmAnd indoor theme.

This is not supposed to be a proper long term solution. Just a temporary better than nothing solution for inspecting current state during survey and experimenting with some aspects of indoor map visualization.


# Features

* Draws indoor rooms, areas, corridors
* Indoor walls
* Filter indoor rooms, shops, amenities by level, level selection using map preferences
* Labels for rooms (name, ref)

# Limitations

* Only simple level assignments `level=x` supported.
* Level ranges or lists not supported `level=x-y` and `level=x;y;z`
* repeat_on not supported
* doesn't interact well with layers
* level [-5; 5] only
* at the time of writing map files provided by osmand lack level=2 due to bug (bug is already fixed but it will take a while until map files include the fix)
* features with unsupported or missing level info will be drawn on all levels, good enough for stairs and elevators that span all levels but can be very noisy in metro stations
* level filtering works only for rooms, shops, common amenities, some footways/corridors and few other object types


# Usage

Copy the xml file to phone and open in OsmAnd. It will add a new theme.

It is recommended to create a separate profile and reorder map configuration menu so that level choice and other indoor shows up at the top.
