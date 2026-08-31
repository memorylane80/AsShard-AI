# System Architecture

## Overview
AsShard-AI is an agentic, multi-tenant SaaS application built for small business local search optimization, review automation, and client acquisition.

## Data & Multi-Tenancy
* **Database:** PostgreSQL managed via Supabase.
* **Tenant Isolation:** Enforced at the database layer using PostgreSQL Row-Level Security (RLS). Every query checks the user's authenticated `company_id`.

## Security & Auth
* **User Authentication:** Supabase Auth via OAuth2.
* **Google Integration:** Secure token storage for Google Business Profile API with encrypted refresh token rotation.
