# NinjaRmmApiExtract
This project extracts information from Ninja RMM and stores it in a SQL database for reporting purposes.

## Credentials
Ninja RMM Account:

## Links
* Authorization: https://app.ninjarmm.com/apidocs/?links.active=authorization#/Endpoints/get_authorize
* API Documentation: https://app.ninjarmm.com/apidocs/?links.active=core
* Device List: /v2/devices-detailed
* Alert List: /v2/alerts

## Data to Store (starter)
* Settings - Key, Name (use for authentication parameters and other settings)
* Organizations - Id, Name
* Devices - Id, Name, OrganizationId, Location, CurrentUser, LastContact, LastUpdate, InServiceDate (Custom Field), IpNumber, 
* Alerts - Id, Name, DeviceId, Severity, Date, Type, Name, Subject

## Requirements
* Do not store ANY account related information in this repo (it is a public repo)
* Database connection string needs to be stored outside of the project as well (but will be needed before we connect to database).
* Console application that will communicate with API to get all devices and alerts from Ninja.
* Currently - will wipe out all existing data and fill with new data each time
* Needs to properly authenticate and store a token to refresh the token on the next run
* Refresh token each time (so it won't expire?)
* Query all devices and store in database (Need to make Organizations as we go and relate devices to them)
* Query all alerts and store in database (Need to relate alerts to devices)

## Future Requirements
* We plan to do reporting using Zoho Analytics.
