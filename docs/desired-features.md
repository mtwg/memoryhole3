# Memoryhole Requirements

Memoryhole is an application for Movement Defense. It is used by NLG lawyers, ground coordinators, incident coordinators, and a wide range of staff and volunteers to track information about defendants who are incarcerated and/or have active cases related to doing social movement work.

## High-level requirements

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




## The Hub Model
  - Information flows in and out from all support roles (see below)
  - <diagram>

### Jail Support/Field Support
  - Jail support users need to look up information on the fly, securely, in sometimes compromised situations (aka outside the jail with police staring at them)
  - Jail support users need to know certain vital information to do their job
  - They will gather information doing on-site support work (meeting with actual arestee, officials, family memebers, etc) and will provide information that is critical to multiple people at once
  - They will often be the first to know if someone is released. If they can just trigger a status change from the field, then hotline folks can call family members and friends with details right away and and then notify lawyers, etc.

### Hotline
  - Hotline users need to enter critical data rapidly
  - Hotline users need to be able to look up profiles rapidly
  - Hotline users need to be encouraged to capture the most critical information first
  - Hotline calls are not always arrestees - more nuanced ways to manage intake of this information (thus tracking 'people' and 'incidents' rather than just always 'arrestees')
  - Will likely be logging conversations and updating information against the same profile concurrently
  - Often are tasked with making outbound calls to gather and disseminate information to family members, support network, friends, and to jail support folks on the ground.
  - Ideally, the application can allow anyone anywhere in the country/world to work the hotlines. The need for hotline workers can scale dramatically.

### Trained Legal Observers
  - Upload evidence from the field
  - Document incidencts with metadata and description
  - Doesn't know any case information
  - Might not know identity of people in incidents
  - Might provide identifying info of people as they get arrested.

### Legal Observers/Trusted Documenters
  - Upload evidence from the field
  - Document incidencts with metadata and description

### Legal Caseworkers
  - Often the most long-term users of this database
  - Stick around after high escalations to handle casework over the long haul
  - Need high-level quantitative reporting
  - Need searching, filtering
  - Need a whole subset of legal case related fields, information, statuses
  - Need to protect attourney/client privelidge
  - Need access to evidence for cases they are working on (wheras other personas are just creating/updating evidence records for a person's profile, or not against their profile at all if identity is unknown by the uploader)
  - Eventually - only assign certain caseworkers to certain cases to protect attourney client priveldge
