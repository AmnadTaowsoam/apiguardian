# APIGuardian Brief

## One-line Summary

Check whether an API is production-ready across contracts, security, errors, rate limits, OpenAPI, versioning, and auditability.

## Category

API Contract / Security Checker

## Priority

Phase 3 / enterprise governance

## Product Context

This project belongs to the public Cerebra Forge Labs / ForgeOps Labs product idea set. The public repository should present APIGuardian as an independent product that people can understand and use, while the deeper Cerebra MCP layer can be used internally for orchestration, review, testing, security, DevOps, and context governance.

## Product Concept

A developer tool that inspects API specifications and live endpoints for endpoint naming, OpenAPI quality, schemas, error formats, auth, rate limits, pagination, idempotency, validation, audit logging, and versioning.

## Why It Should Exist

It is enterprise-friendly and maps to standards that matter for governed platforms: standard error shape, RBAC, audit logs, rate limits, and versioning.

The market need is practical: teams want AI-assisted systems that move beyond prompts and demos into repeatable workflows, validated outputs, and handoff-ready artifacts. APIGuardian should make that workflow explicit and useful from the first release.

## Target Users

backend teams, API platform teams, AppSec engineers, technical leads, integration owners

## Primary Job To Be Done

When a user needs api contract / security checker work, they should be able to provide the minimum required context, run the workflow, inspect the result, and leave with a usable output package rather than vague advice.

## Inputs

OpenAPI file, base URL, auth config, policy profile, sample requests, CI context

## Outputs

API readiness score, contract findings, security findings, breaking-change warnings, policy report

## Core Capabilities

- OpenAPI import
- contract linting
- live endpoint probes
- auth and rate-limit checks
- error shape validation
- pagination/idempotency checks
- audit coverage report
- CI gate mode

## Cerebra MCP Fit

Recommended Cerebra MCP capabilities:

CerebraSecurity-mcp, CerebraReview-mcp, CerebraTesting-mcp, CerebraDevops-mcp

Cerebra should be used as the behind-the-scenes quality layer for role selection, context composition, risk checks, review, testing, security, and delivery evidence. The public product should not require users to understand Cerebra internals before they can get value.

## MVP Experience

1. User creates a project or run.
2. User provides required inputs.
3. System validates missing or risky information.
4. System generates or audits the target artifact.
5. User reviews output, warnings, assumptions, and next steps.
6. User exports or saves the result.

## Differentiation

- Product-specific workflow, not a generic chatbot.
- Concrete outputs that can be committed, deployed, tested, or reviewed.
- Quality gates that make generated work safer to trust.
- Clear traceability from inputs to output.
- Practical public repo structure that invites adoption and contribution.

## Success Metrics

- First useful result is produced in under 10 minutes for a new user.
- At least 80 percent of MVP runs produce an exportable artifact.
- Generated outputs require fewer than three major manual corrections in normal use.
- Users can understand setup and usage from the README without private context.
- The project can be demonstrated publicly with safe sample data.

## Non-goals

- Do not expose private Cerebra internals as a requirement for public use.
- Do not automate destructive or external actions without explicit approval.
- Do not build broad marketplace features before the core workflow works.
- Do not ship AI output without assumptions, risks, and validation status.

## Recommended MVP Stack

OpenAPI 3.1 parser, HTTP probe runner, policy engine, CLI and web report

## Key Risks

probing unsafe environments, false blocking in CI, credential handling, incomplete API inventory

## Launch Recommendation

Ship the first version as a focused public repo with clear docs, sample input, sample output, and a small runnable path. Treat broader integrations as phase two unless they are essential to proving the product.
