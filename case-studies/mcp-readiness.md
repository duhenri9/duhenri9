# MCP Readiness — Agent connectivity engineering

**Project:** WM3 Digital / MCP Readiness  
**Focus:** Model Context Protocol (MCP), agent-ready APIs, identity/tenancy, capability boundaries and delivery evidence  
**Maturity:** Scoped assessment/service path; further visual/commercial work is in unmerged review branches  
**Last reviewed:** 15 October 2026

## The problem

Making an API endpoint callable by an AI agent is only a small part of an enterprise integration. The harder work is deciding **which business capability should be exposed, to whom, with which limits, and how to verify the real effect**.

Teams can adopt MCP too early, mirror all endpoints or conflate tool discovery with business permission.

## What MCP Readiness provides

A bounded architecture and implementation-readiness assessment. Typical deliverables are:

1. Business outcome and workflow map.
2. System, API and identity/tenant inventory.
3. Curated candidate tool/capability map (not an indiscriminate endpoint mirror).
4. READ / WRITE / sensitive / destructive risk and approval matrix.
5. Build-versus-buy and architecture recommendation.
6. Written scope and acceptance criteria for an optional, separately agreed technical delivery.

**An outcome can be a recommendation not to use MCP.** The service is about sound architecture, not selling connectors regardless of fit.

## Engineering approach

~~~text
Business outcome
    → identity and tenant boundary
    → minimal authorised capability
    → policy / approval gate
    → bounded tool execution
    → observable effects and acceptance evidence
~~~

- Authentication is not the same as authorisation.
- Tool metadata and model-produced text do not confer execution permission.
- Retry, idempotency, sensitive operations and failure-handling must be explicitly assessed.
- User-facing claims require contract-backed validation, not mere presence of a connector.
- Requirements move through a structured briefing, scoped review, acceptance and optional delivery.

## Illustrative assessment (not a client claim)

**Request:** Let an assistant update customer records.  
**Risk review:** tenant isolation, role claims, allowed fields, audit events, duplicate writes and human approval for sensitive changes.  
**Possible recommendation:** expose a narrow, role-bound update capability with an explicit postcondition check—or avoid MCP where an existing integration is simpler and safer.

## What exists and what is not yet proved

The WM3 repository contains the current MCP Readiness site route, bounded NEX FAQ/concierge, briefing flow, technical-commercial product truth and a documented review-to-delivery process.

As of 15 October 2026, a premium landing-page revision and Brazilian three-deliverable commercial revision remain in Draft pull requests. These are **not presented here as released functionality, generally available pricing or production-verified outcomes**.

This case study makes no claim of universal client compatibility, production credentials, customer case studies or a fully self-service order portal.

## Roadmap

**Now:** consolidate the approved source of truth, validate the premium UX, test release gates and produce a sanitised sample assessment.  
**Next:** review one bounded implementation against explicit acceptance tests and evidence of effects.  
**Later:** repeatable delivery tooling, integrations and lifecycle support, subject to demand and verification.

**My contribution:** technical/product scope design, architecture review, agent boundaries, test and documentation strategy, multi-model review workflows and translating engineering risk into business decisions.

Private implementation details, internal model instructions, customer systems and unreleased prices are intentionally excluded.

[Back to portfolio](../README.md)
