# Calendar Curator for Google Calendar

Google Calendar makes it difficult to have multiple public
calendars - if someone looks up your public calendar, they
only see the events on your default calendar. If you use
multiple calendars to organize your schedule, this means
not all your events will be visible. Additionally, if you
use a remote calendar (such as iCloud), you can't make any
events publicly show as busy.

This program takes several input calendars and merges them
into on "curated" calendar. It handles event creation, updates,
and deletion. It does this non-destructively by tagging curated
events, so that your gcal invites won't be touched.

It works well when run on a time trigger (such as every night).
It takes betwee 0.5-1.0 seconds per event copied, and so can
generally handle several months or weeks before running into rate limits.

## Configuration

- `daysToCopy` - how far ahead to look from the current date
- `cal_default` - GAS `Calendar` object to copy to
- `cals` - an array of GAS `Calendar` objects to copy from

See the Apps Script [CalendarApp Documentation](https://developers.google.com/apps-script/reference/calendar/calendar-app) for more information.
