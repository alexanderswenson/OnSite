# Onsite

**Delivery and service scheduling software for hot tub and swim spa dealers.**

> From sold to delivered — one system replacing the spreadsheet chaos.

![Status](https://img.shields.io/badge/status-active%20development-blue)
![Stack](https://img.shields.io/badge/stack-React%20%2B%20Supabase-61dafb)

## The Problem

Delivery scheduling at a hot tub dealership runs across **four disconnected tools**: Jotform for site intake, Google Sheets for tracking, Google Calendar for scheduling, and Zapier to glue it all together. Forms get lost, reminders are inconsistent, calendar events fire at the wrong time, and nobody has a single reliable view of what's happening.

I built Onsite to replace all of it with one system.

## What It Does

Onsite manages the full delivery lifecycle — from the moment a sale closes to the moment the unit is installed:

- **Customer Portal** — Mobile-friendly form where customers submit delivery details: address, access path, gate measurements, photos, electrical readiness, pad status
- **Delivery Pipeline** — Internal board tracking every job through status stages: `Submitted → Review Needed → Ready to Schedule → Scheduled → Confirmed → Completed`
- **Google Calendar Sync** — Events created automatically when a job hits "Scheduled," color-coded by status (blue = scheduled, green = confirmed)
- **Automated Reminders** — Email/SMS notifications at 7, 3, and 1 day before delivery
- **Customer Confirmation Workflow** — YES/NO confirmation that auto-updates job status and calendar event

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React (JavaScript) |
| Backend & Database | Supabase (Postgres + Auth + Row Level Security) |
| Calendar Integration | Google Calendar API |
| Notifications | Email/SMS (planned) |
| Hosting | Replit |

## Architecture

```
Customer Portal ──→ Supabase (Postgres + RLS) ──→ Internal Dashboard
                           │
                    Google Calendar API
                           │
                  Automated Reminders ──→ Customer Confirmation ──→ Status Update
```

## Who Uses It

- **Sales staff** — hand off sold jobs into the delivery pipeline
- **Delivery coordinators** — manage scheduling and logistics
- **Managers** — visibility into all pending and completed deliveries
- **Customers** — submit site readiness info and confirm delivery windows
- **Delivery crew** — mobile view of daily schedule (planned)

## Why I Built This

I'm a sales lead at a hot tub dealership. After watching our team lose track of deliveries, double-book installers, and manually chase customers for confirmations, I decided to build the tool we actually needed. Onsite is what happens when the person doing the job builds the software to fix it.

## Status

Active development — multi-tenant architecture and Supabase auth are live, core modules being built.

## License

Private — proprietary software.
