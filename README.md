# EzSeller — agent plugin packages

EzSeller connects authorized Amazon sellers to guided seller-operations workflows through **one hosted MCP server**, independently of the AI assistant.

- Remote MCP: https://ezseller.smatdesigns.com/mcp
- Product and sign-in: https://ezseller.smatdesigns.com
- Developer: SMAT Designs
- Source of actual seller data: account-authorized Amazon Selling Partner access
- Applications: Claude plugins and custom connectors, Gemini CLI, Grok Build and other compatible MCP clients

## Availability and consent

The public EzSeller application is published in ChatGPT. **That is not evidence of listing or approval in Claude, Google, Grok or Cursor.** Amazon's public application approval is separately pending; current seller authorization is limited to approved beta client grants. Availability and entitlement must be checked inside EzSeller. You cannot authorize a seller by installing this plugin alone.

Use your own Amazon and EzSeller authorization flow. Never paste Amazon refresh tokens or internal operator credentials into an AI client. Reads and writes remain tenant-scoped and approval-gated by the hosted service.

## Install and first safe task

The `gemini-extension.json` and `.mcp.json` configure the **same** HTTPS MCP. This repository contains only client-side manifest files and operating instructions; it does not mirror Amazon data or replace EzSeller backend business logic.

After connecting, ask: "Use EzSeller to check my Amazon connection status and identify the authorized marketplace. Do not change any listings." Authenticate only through the official EzSeller OAuth flow.

This plugin is not affiliated with Amazon. Validate returned evidence, permissions and data freshness before acting. For commercial details and support, use the current EzSeller website.
