# Harness IACM Azure Hello World

A minimal Harness IACM pipeline that runs Terraform to provision a simple Azure resource, showing what Harness brings to infrastructure delivery: policy driven governance, built in approvals, and a fully auditable path from plan to apply.

## What this is

A reference example showing how a Harness IACM pipeline is structured: plan, policy check, approval, apply, all backed by Terraform against Azure. The goal is to demonstrate how little scaffolding it takes to get governed, secure infrastructure delivery running end to end.

## Structure

```
.
├── infra/           Terraform config for the Azure resource
├── harness/         Harness IACM pipeline definitions
└── README.md
```

## Pipeline flow

1. Plan — Terraform plan against Azure
2. Policy check — Harness policy as code evaluation
3. Approval — manual gate before apply
4. Apply — provision the resource

## Why Harness

Harness IACM wraps Terraform with the governance and visibility that raw Terraform does not give you out of the box: policy enforcement before anything gets applied, approval gates, drift detection, and a full audit trail of every plan and apply. This repo is a small, honest example of that in action.

## Prerequisites

- Harness account with IACM module enabled
- Azure service principal or connector configured in Harness
- Terraform (or OpenTofu)

## Status

Working reference implementation. Replace the example workspace and Azure configuration with values appropriate to your environment.