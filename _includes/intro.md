# Introduction

Welcome to the CBIS REST API Reference.
If you don't have an API key, visit <a href='http://help.citybreak.com/'>Citybreak Support</a> to get one.

The API is divided into 2 parts, **Raw** and **Localized**. The first one is designed to get all the data we have about something, when the second one is designed to print data in real time.

## Dates and time zones

Every date and time the API returns is in **UTC**, in ISO 8601 with a trailing `Z`, for example `"ExpiresAt": "2018-07-01T01:00:00Z"`. This applies to the Raw and Localized endpoints alike: `ExpiresAt`, `PublishAt`, occasion `Start`/`End` and date/time attribute values (which use the `yyyy-MM-dd HH:mm:ssZ` form).

<aside class="notice">
In the Raw occasions, <code>Start</code> and <code>End</code> are the first and last <b>day</b> of the occasion, with the time of day given separately by <code>StartTime</code> and <code>Duration</code>. That day is expressed as local midnight converted to UTC, so a series starting on 16 June 2016 in Sweden reads <code>"2016-06-15T22:00:00Z"</code>. Convert to your local time zone before taking the date part.
</aside>

Dates you send in filters (<code>After</code>, <code>Before</code>) should include a time zone as well (preferably <code>Z</code>), so they are not open to interpretation.

This documentation is too long? Go play right now with the <a href="https://cbis-rest-api.citybreak.com/v1/swagger/">Swagger UI</a> and come back later.
