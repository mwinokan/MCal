# MCal

Simple command line calendar program for MacOS written in BASH. Each day is broken up into a morning, afternoon, and evening task as well as ```[othN]``` fields which can be used to store small tasks. Each day has an associated text file stored in the data directory.

### Data Directory

Data is stored in "~/Dropbox/MCal/data" by default and is amended on line 6 of the source.

### Usage

- Viewing your calendar

  - ```mcal [relative day]``` display the calendar for the given day. Options are "today", "yesterday", and "tomorrow". Null defaults to today.

  - ```mcal [date]``` display the calendar for the given text file.
  
- Amending a calendar

  - ```mcal add [relative day / file] [field] "[task]"``` Add a given task to the given field of the given date. Relative dates allowed as for viewing. In the case that a field does not exist it is appended. If [field] specified is "all" then [morn], [aftn], and [evng] will be modified.

  - ```mcal mark [relative day / file] [field]``` Toggle completion of an [oth*] field.

  - ```mcal edit [relative day / file]``` Opens the given calendar text file in ```nano```.
