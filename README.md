# Satellite Ephemeris Automatic Download + Transit Event Automatic Output
[中文](./README-zh.md)
## Instructions
After installing the dependencies in `requirements.txt`, simply run `track.py` for the following actions:

1. If `NOARD_ID` is specified in `track.py`, the TLE data will be automatically downloaded from Celestrack. The file will be saved in the `tle` subdirectory of the current directory with a filename of the Unix Timestamp when the script is run.

2. If `latitude` and `longitude` are specified in `track.py`, the script will automatically calculate the transit times of the satellites from the current time to 48 hours later, and output them to a file. The file will be saved in the `events` subdirectory of the current directory with a filename of the Unix Timestamp when the script is run. The threshold elevation angle for transit events is set to 5 degrees by default (consistent with the default behavior of gpredict software), but can be manually modified in `track.py` using the `degrees` variable.

## Example of the output
```
2023-11-15 20:39:54 +08:00 rise above 5°
2023-11-15 20:42:13 +08:00 culminate
2023-11-15 20:44:33 +08:00 set below 5°

2023-11-15 22:11:24 +08:00 rise above 5°
2023-11-15 22:16:01 +08:00 culminate
2023-11-15 22:20:43 +08:00 set below 5°

2023-11-16 09:50:19 +08:00 rise above 5°
2023-11-16 09:54:37 +08:00 culminate
2023-11-16 09:58:53 +08:00 set below 5°

2023-11-16 11:24:55 +08:00 rise above 5°
2023-11-16 11:28:41 +08:00 culminate
2023-11-16 11:32:28 +08:00 set below 5°

2023-11-16 20:30:56 +08:00 rise above 5°
2023-11-16 20:31:38 +08:00 culminate
2023-11-16 20:32:20 +08:00 set below 5°

2023-11-16 22:00:35 +08:00 rise above 5°
2023-11-16 22:05:17 +08:00 culminate
2023-11-16 22:10:04 +08:00 set below 5°

2023-11-17 09:39:55 +08:00 rise above 5°
2023-11-17 09:43:50 +08:00 culminate
2023-11-17 09:47:45 +08:00 set below 5°

2023-11-17 11:13:53 +08:00 rise above 5°
2023-11-17 11:18:03 +08:00 culminate
2023-11-17 11:22:12 +08:00 set below 5°
```