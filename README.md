# Column Calendar

JavaScript DOM calendar event renderer. Currently a work in progress.

[Demo implementation with a Google Apps Script web app.](https://github.com/dwmorrin/gas-columncalendar)

### Goals
* Accepts [iCalendar standard](https://icalendar.org/) events in JSON (or more) formats as input.
* Accepts optional user defined functions for how to display fixed columns and sub-columns.
  * e.g. view columns by calendar, or by location, or by some regex on the descriptions, etc.
  * sub-columns are used when events overlap, and this can be a user defined function as well.

### Usage
```js
// defaults use document.body as the parent element, and default start and end times.
const calendar = new Calendar()

// passing an object with objects allows customization
const calInContainer = new Calendar({container: document.querySelector("#cal_container")})
const calBusinessHours = new Calendar({startingHour: "9AM", endingHour: "5PM"})
```
