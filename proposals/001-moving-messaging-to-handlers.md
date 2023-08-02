**Title**: Moving event generation from hooks to handlers

**Problem Statement**:

Currently when an action is triggered within the Infratographer ecosystem, this is handled via an event hook. 
This works today because we only work with the event triggers that graphql/ent provide us (create|update|delete).
However as we look to introduce lifecycle state to each of our API's, this will begin to complicate such event generation. 
For example, in a world where we have lifecycle states such as (creating|created|updating|deleting|deleted) this doesn't fit into event generation quite as nicely. 
A prime example of this would look something like:
- LB is requested (state=creating,create event is fired)
- LB is created (state=created,update event is fired)
- LB is requested to be deleted (state=deleting,update event is fired)
- Finalizers (TBD) finish cleaning up various LB components (state=deleted, delete event is fired)

The result of this will be (and is currently) a tangled web of overreliance on the message event type and having to predict what state an object is currently in as the event type doesn't actually reflect reality.

**Proposal**:

What we propose is that event generation is moved into the handler itself. In this manner, we can more tightly control when a message is generated. This also allows us to do things like wrapping the entire set of actions within a single transaction which will allow for a cleaner rollback and prevention of sending invalid messages (or because we have better control over the message sending, we would now have better control over things like letting an action complete, regardless if a message fails -- which is in line with how we do things today).

**Potential Drawback**:

Some of the information that is available to us in hooks that we use to craft change messages may not necessarily be available to us (or at least as easily available to us) inside of the handlers. Further investigation/discussion may be required as to the importance of this.
