## Title

## The Hub
  - Information flows in from all support roles
  - <diagram>

## User Personas: Jail Support/Field Support
  - Jail support users need to look up information on the fly, securely, in sometimes compromised situations (aka outside the jail with police staring at them)
  - Jail support users need to know certain vital information to do their job 
  - They will gather information doing on-site support work (meeting with actual arestee, officials, family memebers, etc) and will provide information that is critical to multiple people at once
  - They will often be the first to know if someone is released. If they can just trigger a status change from the field, then hotline folks can call family members and friends with details right away and and then notify lawyers, etc.
  
## User Personas: Hotline
  - Hotline users need to enter critical data rapidly
  - Hotline users need to be able to look up profiles rapidly
  - Hotline users need to be encouraged to capture the most critical information first
  - Hotline calls are not always arrestees - more nuanced ways to manage intake of this information (thus tracking 'people' and 'incidents' rather than just always 'arrestees')
  - Will likely be logging conversations and updating information against the same profile concurrently
  - Often are tasked with making outbound calls to gather and disseminate information to family members, support network, friends, and to jail support folks on the ground.
  - Ideally, the application can allow anyone anywhere in the country/world to work the hotlines. The need for hotline workers can scale dramatically.
  
## User Personas: Trained Legal Observers
  - Upload evidence from the field
  - Document incidencts with metadata and description
  - Doesn't know any case information
  - Might not know identity of people in incidents
  - Might provide identifying info of people as they get arrested.
  
## User Personas: Legal Observers/Trusted Documenters
  - Upload evidence from the field
  - Document incidencts with metadata and description

## User Personas: Legal Caseworkers
  - Often the most long-term users of this database
  - Stick around after high escalations to handle casework over the long haul
  - Need high-level quantitative reporting
  - Need searching, filtering
  - Need a whole subset of legal case related fields, information, statuses
  - Need to protect attourney/client privelidge
  - Need access to evidence for cases they are working on (wheras other personas are just creating/updating evidence records for a person's profile, or not against their profile at all if identity is unknown by the uploader)
  - Eventually - only assign certain caseworkers to certain cases to protect attourney client priveldge

## Core Needs: Stability & Access
  - No downtime or call latency! *Only* land lines (for now)
  - (Non Tech) Operations support must provide resources for land lines
    - with round-robin dialing
    - that supports collect calls
  - *Future:* Custom VOIP/webrtc implementation
    - Automate lookup of inbound caller
    - Easily & Securely record calls
    - "Cloud" availability & distributed hotline

## Core Needs: Anywhere, Anytime
  - 

## Core Needs: Scale up
  - High availability when the actions are happening
  - Support potentially hundreds of users at the same time
  - Automated remote backup
 
## Core Needs: Scale down
  - Scale down for long term support and casework
  - Not as much need for concurrent editing
