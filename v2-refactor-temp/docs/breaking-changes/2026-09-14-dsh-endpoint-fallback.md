---
title: DSH uses compatible fallback endpoints without requiring the local gateway
category: changed
severity: notice
introduced_in_pr: '#19217'
date: 2026-09-14
---

## What changed

DSH now connects through the compatible endpoint that made a model available in the picker, including a later declared endpoint or the provider default. These models no longer unexpectedly require the local API Gateway or fail as unsupported.

## Why this matters to the user

Models whose first endpoint is unsupported by DSH can use a compatible fallback with the provider's existing credentials and URL settings.

## What the user should do

Nothing — automatic.

## Notes for release manager

This completes the DSH runtime handling for #19217. Providers with no native DSH protocol still use the existing gateway fallback.
