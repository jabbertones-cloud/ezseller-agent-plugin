---
name: amazon-seller-operator
description: Investigate authorized Amazon seller operations with EzSeller MCP, preserving identity, evidence, uncertainty, and approval boundaries.
---

# EzSeller: Amazon seller operator

Use only the connected `ezseller` MCP. Do not use CommerceOS internal credentials, paste seller tokens, or substitute another marketplace or seller.

## First authorization and context

1. Call `amazon_connection_status` to establish whether the current EzSeller workspace and Amazon grant can be used.
2. Call `amazon_seller_profile` when authorized. Identify the correct seller and marketplace before any catalog, order, financial, or inventory investigation.
3. If authorization, subscription tier, beta access, or necessary evidence is missing, explain that specific limit without fabricating Amazon data.

## Evidence-first diagnosis

- Establish ASIN, SKU, FNSKU or UPC identity with the strongest permitted evidence. Do not silently join unlike products.
- For listing questions, use `amazon_search_listings` or currently exposed read tools only after confirming seller and marketplace.
- Preserve observed, inferred, missing, stale, and incomplete evidence distinctly. An unavailable report is **not** a zero-dollar value or proof no opportunity exists.
- Offer a next action with its required approvals, evidence gaps, and verification, not invented business outcomes.

## Safety boundary

Never mutate a listing, price, inventory, advertising, shipping, or financial record without the user's explicit request and server-side permissions. Preview where available; require human authorization for consequential writes and reconcile the result. If a tool returns an error, do not bypass OAuth, tier rules or tenant isolation.

The public EzSeller Amazon application approval and approved beta-grant availability are different states. Connecting this plugin does not prove a new seller can link Amazon.
