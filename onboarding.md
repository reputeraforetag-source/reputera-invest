# Reputera Onboarding Workflow

**Status:** Fully Automated  
**Integration:** FluentCRM to PMS  
**Purpose:** Automated customer onboarding from payment to portal access

---

## Overview

This document describes the complete onboarding flow for Reputera customers, from initial payment to full dashboard access.

---

## Customer Flow Diagram

```mermaid
graph TD
    A[Visit premiarkund] --> B[Choose plan]
    B --> C[PayPal payment]
    C --> D[Subscription created]
    D --> E[FluentCRM automation]
    E --> F[Welcome emails]
    F --> G[Onboarding wizard]
    G --> H[Portal access]
Process Steps
1. Customer Visit
Customer visits the premiarkund page

Selects Solo or Tillvaxt plan

2. Payment
Payment completed via PayPal

Payment confirmation sent to PMS

3. Subscription Creation
PMS creates subscription

Automation file runs:

reputera-welcome-automation.php

Tags added in FluentCRM:

new-customer

plan-solo or plan-tillvaxt

welcome-sequence

onboarding-pending

payment-confirmed

4. Welcome Email Funnel
Four automated emails:

Welcome and onboarding start

First actions to complete

SMS usage reminder

Help and support message

5. Onboarding Wizard
Customer completes required steps:

Company information

Business type

Google Business setup

Customer flow settings

Test SMS confirmation

Access to the portal is blocked until completion.

6. Onboarding Completion
Triggered file:

onboarding-fluentcrm-hook.php

FluentCRM updates:

Add onboarding-completed

Remove onboarding-pending

Save company and business type fields

7. Portal Access
Customer gains access to:

SMS system

Analytics dashboard

Customer management

Plan-specific features

Automation Benefits
No manual handling

Full customer journey tracking

Scalable onboarding

Consistent customer experience

Technical Files
File	Purpose
reputera-welcome-automation.php	Payment to CRM sync
onboarding-fluentcrm-hook.php	Onboarding completion sync

Metrics to Track
Activation rate

Time from payment to portal

Onboarding completion rate

Email engagement

