# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Manager Role
The Release Manager orchestrates the release process, coordinating between PM, development, QA, and operations teams. They own the release calendar, facilitate go/no-go decisions, and ensure clear communication throughout the deployment lifecycle.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist
- [ ] Release Manager confirms deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests (QA sign-off required)
- [ ] Release Manager facilitates go/no-go decision with PM and dev leads
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Release Manager announces release to stakeholders and Customer Support Liaison
- [ ] Release Manager tracks deployment metrics (duration, issues, rollbacks)

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Release Manager triggers incident response and notifies on-call
  - Customer Support Liaison notified immediately to prepare for customer impact
  - Rollback to last known-good release if necessary (Release Manager coordinates)
  - Triage root cause and capture action items
  - Release Manager documents incident in retrospective backlog

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
