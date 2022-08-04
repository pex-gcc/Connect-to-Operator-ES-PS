# Event Sink & External Policy Server for Pexip Infinity

The EventSink function listens for all events coming from Pexip.  It then sends messages along to message queues to be handled.  The QueueAllEvents function puts all events into the 'events' database, with unique IDs generated by Cosmos and `event_type` as partition key.

Necessary environment variables:

```
DatabaseEndpoint        - endpoint for Azure Cosmos database for storing all events and active calls
QueueStorageAccount     - endpoint for storage account for queues
EventsDatabaseName      - name of the database with Cosmos to store events 
EventsContainerName     - name of the container within the above database to store events
```