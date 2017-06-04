

## High-level Features

At a high level, the requirements are very much like any case management system, with some specifics.

### Data Model
- Nuanced Data model with lots of relations between models
- Usually a lot of many-to-many relationships (thus not optimal for NoSQL, likely)
- Highly flexible custom fields to be added to any object in the data model
- Revision management with a changelog for every field and record

### API
- A flexible API for allowing external bots and scripts
- Update records using a bot that scrapes court dockets

### Reporting & Exports
- Nuanced reporting mechanisms
- Be able to build reports based on intricate search conditions across multiple related objects
- Provide metrics for large-scale mobilizations
- Provide 'live queries' aka 'smart groups' of active cases that meet certain conditions (ala CiviCRM)
- Provide flexible exports (CSV, XLS, PDF)

### Stability & Access
- Automated remote backups with automated confirmation (ideally, also a failover instance that is constantly monitored to be working)
- DDOS mitigation measures (DNS (i.e. Cloudflare), "serverless", hosting providers)
-

### Anywhere, Anytime
- Ideally, could be run off a laptop over a local network, maybe use ngrok to forward 443 out over a tor hidden service

### Scale up
- High availability when the actions are happening
- Support potentially hundreds of users at the same time

### Scale down
- Scale down for long term support and casework
- Not as much need for concurrent editing

### Security, Privacy & Access Control
- HIPAA-level security - encrypted at rest and in transit ALWAYS (including on the client)
- Should not cache decrypted data in client devices
- Backend needs to be as zero knowledge as possible
- Protect Attorney/Client privelidge
- User and group-based access to arestee, cases, contact information, personal information
- Limit access on a per-user and per-field basis if possible
- For example, ground coordinators/onsite support folks may know personal information & contact information, but have limited access to case information

### Accessibility & Internationalization
- Needs to be translateable to any language, eventually
- Usable in the field, on-site (), with limited or no network access
