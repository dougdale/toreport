# toreport

Generate a time off report from an iCal online calendar. Full days are treated as 8 hours of time off while partial day entries use the length of the calendar entry.

A YAML configuration file (toreport.yaml, by default) specifies the calendar URL, the year of interest, and the 'types' of time off entries in the calendar.

Format:
```yaml
url: <calendar URL>
year: 2021
types:
  "Work PTO":
    available: 120
  "Work Personal Holiday":
    available: 16
```

In the 'types' map, the key value string is the string that the script searches for in the calendar to find entries. The 'avaialble' value is the total number of hours of time off of that type that are available at the start of the year.
