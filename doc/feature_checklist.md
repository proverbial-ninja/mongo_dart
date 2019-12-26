# Functionality Checklist

From [Feature Checklist for Mongo Drivers](http://www.mongodb.org/display/DOCS/Feature+Checklist+for+Mongo+Drivers)

## Essential
- [x] BSON serialization/deserialization: 
- [x] Basic operations: query, insert, update, remove, ensureIndex, findOne, limit, sort: 
- [x] Fetch more data from a cursor when necessary (dbGetMore): 
- [x] Sending of KillCursors operation when use of a cursor has completed (ideally for efficiently these are sent in batches): 
- [x] Convert all strings to utf8: 
- [x] Authentication: 

## Recommended

- [x] automatic _id generation: 
- [ ]  Database $cmd support and helpers
- [x] Detect { $err: ... } response from a db query and handle appropriately --see Error Handling in Mongo Drivers 
- [ ] Automatically connect to proper server, and failover, when connecting to a Replica Set
- [ ] ensureIndex commands should be cached to prevent excessive communication with the database. (Or, the driver user should be informed that ensureIndex is not a lightweight operation for the particular driver.)
- [ ] Support detecting max BSON size on connection (e.g., using buildinfo or isMaster commands) and allowing users to insert docs up to that size.


## More Recommended

- [x] lasterror helper functions: 
- [x] count() helper function: 
- [x] $where clause: 
- [ ] eval()
- [x] File chunking (GridFS) 
- [x] hint fields 
- [x] explain helper 

## More Optional

- [ ] addUser, logout helpers
- [ ] Allow client user to specify Option_SlaveOk for a query
- [ ] Tailable cursor support
- [ ] In/out buffer pooling (if implementing in a garbage collected languages)

## More Optional

- [ ] connection pooling
- [ ] Automatic reconnect on connection failure
- [ ] DBRef Support:
 - [ ] Ability to generate easily
 - [ ] Automatic traversal
