# Tableau MCP deployment guide

A short, practical guide to self-hosting the [Tableau MCP server](https://github.com/tableau/tableau-mcp)
next to your Tableau Server, so everyone in your organization can use Claude Code or Cursor with
Tableau, each signed in as themselves (per-user OAuth, no shared credentials).

**Read it:** [index.html](index.html) — open it in a browser, or view the published page at
<https://laviDrori0702.github.io/tableau-mcp-deployment-guide/>.

## What it covers

1. The values you need (placeholders with fictional examples)
2. Prerequisites: Tableau Server 2025.3+, Node.js 22.7.5+, a TLS certificate
3. Setup: install, OAuth signing key, `tsm` redirect host, certificate, `.env`, first run
4. Running it at boot as a Windows scheduled task
5. Connecting Claude Code and Cursor
6. Troubleshooting by symptom

The examples are for a Windows host. Every hostname and value is a placeholder.

## Not official

This is a community guide, not a Tableau document. For the full reference (Docker, Linux, every
environment variable) see Tableau's own
[deployment guide for Tableau Server](https://github.com/tableau/tableau-mcp/blob/main/docs/docs/enterprise/tableau-server.md).
