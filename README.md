# ministersconsultationresponse
Signatories to the "[Church Ministers' response to the Consultation on Banning Conversion Therapy](https://web.archive.org/web/20220216103235/https://ministersconsultationresponse.com/signatories/)", parsed [from the PDF](https://web.archive.org/web/20220215102757/https://ministersconsultationresponse.com/wp-content/uploads/2022/01/Dear-Secretary-of-State-Letter-from-2546-signatories-to-the-consultation-on-banning-conversion-therapy.pdf).

## signatories.json ([view](signatories.json))
This JSON file contains all 2546 signatories (`name` and `org`) of the consultation in the following format:
```json
{
  "1": {
    "name": "Pastor Mohan Abbadasari",
    "org": "Minister of Religion, New Life SDA Church, Seventh-day Adventist."
  }
}
```

## signatories_with_addresses.json ([view](signatories_with_addresses.json))
This JSON file contains all 2546 signatories (`name`, `org` and `address`) of the consultation in the following format:
```json
{
  "1": {
    "name": "Pastor Mohan Abbadasari",
    "org": "Minister of Religion, New Life SDA Church, Seventh-day Adventist.",
    "address": "10 Lennox Rd, Finsbury Park, London N4 3NW, UK"
  }
}
```

### Please note
To get the addresses, I ran the `org`s through some validation and then through [Google's Geocoding API](https://developers.google.com/maps/documentation/geocoding?hl=en_GB)—some `org`s returned no results, or did not have enough information to provide a useful address. To mark this, I've used the following:
 - `[?]` - did not pass a normal UK address validator, but confident its an address
 - `[??]` - did not pass a normal UK address validator, not very confident its an address
 - `!bad_api_response!` - the Google API returned no results (or another error)
 - `!cannot_parse_org!` - the `org` could not be parsed into anything useful to search with
