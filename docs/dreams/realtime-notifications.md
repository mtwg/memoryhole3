# Realtime Push Style Notifications

Movement defense work often comes down to the minute when it comes to coordinating support and cases.

Information received in a hotline call or from someone calling facilities (offsite) could be vital to those providing onsite support.

Currently, when a key update for a case or an arrestee's status comes through, the signal text loops and calls come alive and many people must update eachother in what could be described as a "manual" fashion.

## Features
- Application wide notification settings
- Role-wide notification settings
- Per user configurable settings
- Privacy & Security features by default:
  - If it's ever an actual mobile push notification, the information is limited, i.e. "An Arestee's Information Has Been Updated" or "An Arestee Has Been Released". Notification messages should never reveal protected information or attorney client privelidged information.
  - Always encrypted end to end
  - Not using a third party to push notifications (even metadata is a concern)

## Implementation Thoughts

- Since all support roles are using Signal, this may be an existing, encrypted channel for disseminating notifications (see: OWS riseup list discussions for bots/API messages)
- Email is also fine if we leverage a riseup <> riseup SMTP (whitelist domains) or are able to use GPG behind the scenes somehow (only send notifications to emails with an available GPG on the keyserver, or uploaded GPG pubkey)
