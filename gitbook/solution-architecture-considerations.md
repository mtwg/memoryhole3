## Offline Storage?

This determines a lot of our solution architecture considerations. Offline storage is complicated because it necessitates many clients synchronizing back and forth with a shared data store. PouchDB/CouchDB make this pretty straightforward to implement.

### How necessary is it
- There isn't a lot of data to synchronize

#### Pros of no offline storage:
- Much simpler to implement
- Data lives at rest only on server over HTTPS and/or tor hidden services
- Only data persisted on client is JWT authorization token which can be stored in cookie or localstorage, whichever the mobile browser of choice supports, if any. In my experience storing JWT tokens in cookies were supported by HIPAA but only out of familiarity with audit team, not based on actual security considerations.

#### Cons of no offline storage:
- Limited 3G/4G access
- In order to log in, a user may still need to reduce the security of Orfox browser, etc.

### What are our requirements & limitations

## Addressing the application
- Normal hostname over HTTPS OR tor hidden services only?

## Authentication && Authorization

### Our own Oauth2 server?

### LDAP?

### Web Client Considerations:

#### JWT
- [Stop using JWT for sessions](http://cryto.net/~joepie91/blog/2016/06/13/stop-using-jwt-for-sessions/)
- [Stop using JWT for sessions, part 2: Why your solution doesn't work](http://cryto.net/~joepie91/blog/2016/06/19/stop-using-jwt-for-sessions-part-2-why-your-solution-doesnt-work/)
