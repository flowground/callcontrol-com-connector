# ![LOGO](logo.png) Call Control **flow**ground Connector

## Description

A generated **flow**ground connector for the Call Control API (version 2015-11-01).

Generated from: https://api.apis.guru/v2/specs/callcontrol.com/2015-11-01/swagger.json<br/>
Generated at: 2019-06-06T16:12:02+03:00

## API Description

API for blocking phone calls with Call Control. Data is from crowdsourced community blacklist from 12+ million users and government agencies (FTC, FCC, IRS) Try with api_key 'demo', hit explore above, and then try phone numbers 18008472911,13157244022,17275567300,18008276655,12061231234.

## Authorization

Supported authorization schemes:
- API Key
## Actions

### Complaints: Free service (with registration), providing community and government complaint lookup by phone number for up to 2,000 queries per month.  Details include number complaint rates from (FTC, FCC, IRS, Indiana Attorney  General) and key entity tag extractions from complaints.

> This is the main funciton to get data out of the call control reporting system<br /><br/>
>             Try with api_key 'demo' and phone numbers 18008472911, 13157244022, 17275567300, 18008276655, and 12061231234 (last one not spam)

*Tags:* `Complaints`

#### Input Parameters
* `phoneNumber` - _required_ - phone number to search

### Enterprise  GET: GetUser<br/>
> Returns the current information from the user;  try 12066194123 as demo

*Tags:* `EnterpriseApi`

#### Input Parameters
* `phoneNumber` - _required_

### Enterprise  GET: ShouldBlock<br/>
> Simple Enteprise which returns a call block proceed decision.

> This returns information required to perform basic call blocking behaviors<br/>
>             Try with api_key 'demo' and phone numbers 18008472911, 13157244022, 17275567300, 18008276655, and 12061231234 (last one not spam)

*Tags:* `EnterpriseApi`

#### Input Parameters
* `phoneNumber` - _required_ - phone number to search
* `userPhoneNumber` - _required_ - (OPTIONAL) phone number of user to look up block rules

### UpsertUser: insert or update all properties from a user<br/>
> PhoneNumber<br/>
> WhiteList (list of phone numbers to whitelist)<br/>
> BlackList (list of phone numbers to blacklist)<br/>
> QuietHourList (list of quiet hour objects)<br/>
> UseCommunityBlacklist (enable / disable community blacklist) default true<br/>
> BreakThroughQhWithMultipleCalls (break through quiet hours with two calls in 3 minutes)<br/>
> WhiteListBreaksQh (break through quiet hours for whitelist)

*Tags:* `EnterpriseApi`

### Report: report spam calls received to better tune our algorithms based upon spam calls you receive

> This returns information required to perform basic call blocking behaviors<br /><br/>
>             Try with api_key 'demo' and phone numbers 18008472911, 13157244022, 17275567300, 18008276655, and 12061231234 (last one not spam)

*Tags:* `Reputation`

### Reputation:<br/>
> Premium service which returns a reputation informaiton of a phone number via API.

> This returns information required to perform basic call blocking behaviors<br /><br/>
>             Try with api_key 'demo' and phone numbers 18008472911, 13157244022, 17275567300, 18008276655, and 12061231234 (last one not spam)

*Tags:* `Reputation`

#### Input Parameters
* `phoneNumber` - _required_ - phone number to search

## License

**flow**ground :- Telekom iPaaS / callcontrol-com-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
