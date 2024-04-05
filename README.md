# eventcatalog
## Usage
- Helps you to document your event driven architecture
- Document and capture your events, services, domains, schemas, code and examples
- It is pluggable
- View versions of Events with changelogs
- Integrated with OpenAPI


## About Terminology
### Events Catalog
    Event Catalog is a top-level term for the Schema Registry (repository), Schema Registry API and documentation site functionality.
### Event
    Event is created by producer / publisher and it contains information about a change in state (e.g. FeedbackCreated). Interested consumers can subscribe / listen these events.

### Domain
    EventCatalog allows you to group your events and services by your application domains.

### Services
    Services are also known as your events Producers or Consumers.


### Event Scehma
    Event schema is a specification of the structure of the event. Schema determines all fields in event.


## Key Points
- EventCatlaog uses NextJS under the hood. 

## Start creating your event catalog project
- Scaffold project website

```code
npx @eventcatalog/create-eventcatalog@latest my-catalog
```

- Project structure
    - **services** - Contains the service Markdown files within your Architecture. 
    - **events** - Contains your Event-Driven Architecture Events. These folders and files can contain markdown, schemas and much more
    - **static**- Static directory. Any contents inside here will be copied into the root of the final build directory. You can add your own logo here and favicon. 
    - **/eventcatalog.config.js** - A config file containing the site configuration. Read the API docs

- Run
```code
npm run dev
```

**EventCatalog** provides many features while documenting your events
 - Schema - Renders code snippets of your Schemas (Supports any schema)
 - Code Examples - Give developers code examples of how to use your Events (Supports any language)
 - Owners - Document owners of your events so teams know who owns what
 - Producers - Document producers of your events
 - Consumers - Document consumers of your events
 - Versions - Version your event, schema, and more!

## Adding Events to your EventCatalog
You will find all events within the /events directory.

To add a new event you will need to create a new folder with your event name and an index.md file inside that folder.

/events/{Event Name}/index.md
(example /events/UserSignedUp/index.md)

Once you create your new file you will need to fill it with the event front-matter data and markdown content.

**There are two parts of the event data**
 - event configuraiton (fontmatter)
 - content (markdown)

## Deployment
```code
npm run build
```
This will output two directories

out - Your EventCatalog as Static HTML (recommended to use)
.next - If you wish to deploy to NextJS (NextJS outputs this by default, recommended to use the out directory)

## Links
https://www.eventcatalog.dev/docs/introduction
https://www.kallemarjokorpi.fi/blog/how-to-create-and-event-catalog.html

Use Netlify to host static web site
https://www.netlify.com/blog/2016/10/27/a-step-by-step-guide-deploying-a-static-site-or-single-page-app/