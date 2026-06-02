# Scaffold SupportOps API

We are building SupportOps, a small multi-tenant support ticket application for a GitHub Copilot hackathon.

Create the first working .NET 8 minimal API slice.

The attendee is the driver and reviewer. Copilot should generate the first draft, but the attendee must run, inspect, and explain the result before moving on.

## Requirements

- Use .NET 8 minimal APIs.
- Keep the structure simple and easy for attendees to understand.
- Add a `Ticket` model with:
  - `Id`
  - `TenantId`
  - `Subject`
  - `Description`
  - `Status`
  - `Priority`
  - `CreatedAt`
- Seed 5 sample tickets in memory.
- Add `GET /health`.
- Add `GET /tickets`.
- Add `GET /tickets/{id}`.
- For now, keep storage in memory. Do not add a database.
- Explain the files you create.

## Implementation Guidance

- The `Ticket` model can be a simple C# record or class.
- The in-memory ticket store can be a `List<Ticket>` seeded in `Program.cs` for Activity 1.
- Seed tickets should include at least two tenants, for example `acme` and `globex`.
- `GET /tickets/{id}` should return `404 NotFound` when the ticket does not exist.
- Do not add authentication, a database, repository classes, service layers, or UI in Activity 1.
- After creating the code, explain how an attendee can run and test it.

## Acceptance Criteria

- The app runs locally.
- `GET /health` returns a healthy response.
- `GET /tickets` returns seeded tickets.
- `GET /tickets/{id}` returns one ticket when it exists.
- The code is simple enough to explain in a hackathon.