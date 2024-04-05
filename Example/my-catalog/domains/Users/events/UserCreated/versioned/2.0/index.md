---
name: UserCreated
version: 2.0
summary: |
    When user is created event
producers:
    - User Service
consumers:
    - Email Service
owners:
    - bhoopal
---

<NodeGraph title="UserCreated Event" />

<Schema title="UserCreated Schema" />

<SchemaViewer title="Event data properties" renderRootTreeLines maxHeight="500"/>


## OpenAPI Schema

OpenAPI schema for the event can be found below.

<OpenAPI  />

<EventExamples title="How to trigger event" />