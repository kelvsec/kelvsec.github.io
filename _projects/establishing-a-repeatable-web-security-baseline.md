---
title: Establishing a Repeatable Web Security Baseline
description: A practical framework for recording and reviewing the visible security posture of a web property.
date: 2026-07-01 10:00:00 +0100
status: Complete
categories:
  - Web security
tags:
  - security headers
  - methodology
  - defensive security
---

A useful security baseline is a dated, repeatable record of how a system appears before changes are made. It gives defenders something concrete to compare against later.

## Scope and approach

For a public website, a lightweight baseline can record DNS configuration, TLS behaviour and HTTP response headers. Only assess systems you own or have explicit permission to test.

```text
baseline/
├── dns.txt
├── headers.txt
└── notes.md
```

Keep the collection method consistent, note the time of observation and document redirects. A baseline is not a complete security assessment; it is an inventory of observable facts that supports further review.

## What to record

1. The canonical hostname and redirect path.
2. The certificate issuer, validity window and covered hostnames.
3. Security-relevant response headers.
4. Any expected third-party resources or external origins.

Repeat the process after a material change. Differences can then be reviewed intentionally rather than discovered accidentally.
