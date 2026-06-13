# Sunrise Sunset

Free REST API providing sunrise, sunset, solar noon, day length, and civil, nautical, and astronomical twilight times for any geographic location and date.

No API key or account is required. Attribution to [sunrise-sunset.org](https://sunrise-sunset.org/) is required when using the API.

## API

**Base URL:** `https://api.sunrise-sunset.org/json`

**Method:** GET

### Parameters

| Parameter | Type | Required | Description |
|-----------|------|----------|-------------|
| `lat` | float | Yes | Latitude in decimal degrees |
| `lng` | float | Yes | Longitude in decimal degrees |
| `date` | string | No | Date in YYYY-MM-DD format (defaults to today) |
| `formatted` | integer | No | 0 or 1 (default: 1); affects time format |
| `tzid` | string | No | Timezone identifier (e.g., UTC, America/New_York) |
| `callback` | string | No | JSONP callback function name |

### Example Request

```
GET https://api.sunrise-sunset.org/json?lat=36.7201600&lng=-4.4203400&date=2026-06-13
```

### Example Response

```json
{
  "results": {
    "sunrise": "6:12:03 AM",
    "sunset": "8:33:11 PM",
    "solar_noon": "1:22:37 PM",
    "day_length": "14:21:08",
    "civil_twilight_begin": "5:44:14 AM",
    "civil_twilight_end": "9:01:00 PM",
    "nautical_twilight_begin": "5:10:15 AM",
    "nautical_twilight_end": "9:34:59 PM",
    "astronomical_twilight_begin": "4:33:43 AM",
    "astronomical_twilight_end": "10:11:31 PM"
  },
  "status": "OK",
  "tzid": "UTC"
}
```

## Links

- **Website:** https://sunrise-sunset.org/
- **API Documentation:** https://sunrise-sunset.org/api
- **Status Page:** https://apistatus.sunrise-sunset.org/
- **Terms of Use:** https://sunrise-sunset.org/terms
- **Privacy Policy:** https://sunrise-sunset.org/privacy
- **Contact:** https://sunrise-sunset.org/contact

## APIs.json

This repository contains an [APIs.json](apis.yml) profile cataloging the Sunrise Sunset API as part of the [API Evangelist](https://apievangelist.com) network.
