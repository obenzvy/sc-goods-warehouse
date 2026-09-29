# SC Goods Warehouse Portal

Static frontend for the SC Goods Warehouse system.

## Hosting
Designed for GitHub Pages. Serve `index.html` from the repository root.

## Backend
The portal connects directly to the SC Goods Warehouse Supabase project using a publishable browser key. No Supabase secret/service-role key is included in this repository.

## Security model
- GitHub Pages serves only static HTML/JavaScript.
- Supabase Auth handles sign-in.
- Database tables are not directly exposed to browser users.
- The browser can call only approved Supabase RPC functions.
- Owner-only RPCs enforce Owner role checks server-side.
- Owner financial data remains in owner-only database paths.

## Measurement rules
- Warehouse-entered **individual sellable item** dimensions/weight can be compared with Amazon item/package measurements.
- Warehouse-entered **casepack/master carton** dimensions/weight are operational data only and are not compared with Amazon catalog dimensions.

## Current version
v0.3.0 — GitHub Pages frontend, Supabase backend.
