# Twenty CRM API Documentation

## Overview

Twenty CRM (twentyhq/twenty) is an open-source CRM solution that can be self-hosted. Based on the provided documents, here's what we know about the API:

- The API appears to use a combination of REST and GraphQL endpoints
- Authentication is done via API keys (Bearer tokens)
- The system follows standard CRUD operations for the main objects

## Core Objects

Based on the documentation in `twentyCRMforStruktive.md`, the main objects in Twenty CRM include:

- **Companies** - Clients and organizations
- **People** - Contacts associated with companies
- **Opportunities** - Sales pipeline deals
- **Tasks** - Action items associated with companies or contacts
- **Notes** - Documentation added to various objects
- **Activities** - Timeline of interactions

## API Authentication

Authentication appears to be token-based. Based on the information provided, you would likely:

1. Generate an API key in the Twenty CRM interface
2. Include it in request headers as a Bearer token:
   ```
   Authorization: Bearer YOUR_API_KEY
   ```

## GraphQL API

The system likely uses GraphQL for more complex operations. This would typically be accessible at an endpoint like:

```
https://your-instance/graphql
```

GraphQL would allow querying specific fields and relationships in a single request.

## REST Endpoints

The REST API would likely follow standard patterns for CRUD operations:

- `GET /api/companies` - List companies
- `GET /api/companies/:id` - Get a specific company
- `POST /api/companies` - Create a new company
- `PATCH /api/companies/:id` - Update a company
- `DELETE /api/companies/:id` - Delete a company

Similar patterns would exist for people, opportunities, etc.

## Integration Points

For your Struktive implementation, you'd likely want to focus on:

1. **Client Management APIs** - Adding/updating clients in Twenty CRM
2. **Activity Logging** - Recording client interactions
3. **Task Management** - Creating and updating tasks for deliverables
4. **Note Storage** - Saving project documentation within the CRM

## Webhook Support

The documents mention tracking timeline activities, which suggests Twenty CRM may support webhooks for real-time updates. If available, this would be useful for:

- Triggering actions when tasks are completed
- Updating external systems when notes are added
- Alerting team members about new opportunities

## Next Steps

To fully document the Twenty CRM API for your implementation:

1. Check the official Twenty CRM documentation
2. Look for API documentation in the GitHub repository
3. Examine the actual source code to identify endpoints
4. Create a test instance and use browser developer tools to observe API calls
5. Test endpoints with tools like Postman to confirm functionality

Since Twenty is open-source, you can always examine the source code directly for the most accurate API information.
