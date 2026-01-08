# Data Privacy & GDPR Compliance – Reputera

## Executive Summary

Reputera is built with **Privacy by Design** principles from the ground up. As a Swedish company processing personal data (reviews contain personal information), we take GDPR compliance seriously and have implemented comprehensive data protection measures that exceed industry standards.

## Legal Framework

### Applicable Regulations
🇪🇺 Primary Regulations:
• EU General Data Protection Regulation (GDPR)
• Swedish Data Protection Act (Dataskyddslagen)
• ePrivacy Directive (cookies and electronic communications)

🇸🇪 Swedish Specific:
• Marketing Act (Marknadsföringslagen)
• Electronic Communications Act (LEK)
• Consumer Services Act (Konsumenttjänstlagen)

text

### Data Controller vs Processor
👥 Our Role: Data Processor
• Our customers (businesses) are Data Controllers
• We process personal data on their behalf
• We have Data Processing Agreements (DPAs) with all customers

📝 Customer Responsibility:
• Obtain proper consent from their customers
• Provide privacy notices
• Handle data subject requests

text

## Data Processing Overview

### Types of Data Processed
📋 Customer Data (Business Users):
• Business information (name, address, contact details)
• Employee/user account information
• Payment information (processed by Stripe)

👤 End Customer Data (Review Authors):
• Name (as provided in reviews)
• Contact information (phone, email for SMS/email triggers)
• Review content and ratings
• Metadata (time, date, platform)

🔍 Technical Data:
• IP addresses
• Device information
• Usage analytics (anonymized)
• Log files

text

### Data Flow Architecture
🔀 Data Collection Points:

Customer onboarding (business information)

Review collection (end customer data)

Platform usage (technical data)

Third-party integrations (Google, Facebook APIs)

🛡️ Security Measures at Each Stage:
• Encryption in transit (TLS 1.3)
• Encryption at rest (AES-256)
• Access controls (Role-Based Access Control)
• Audit logging

text

## GDPR Compliance Implementation

### Article 5 Principles
✅ Lawfulness, fairness, transparency:
• Clear privacy policy
• Transparent data processing descriptions
• Legal basis for all processing

✅ Purpose limitation:
• Data collected only for specified purposes
• No secondary processing without consent

✅ Data minimization:
• Only collect necessary data
• Regular data clean-up procedures

✅ Accuracy:
• Customers can update their information
• Review data comes directly from platforms

✅ Storage limitation:
• Automatic deletion schedules
• Review data retained as long as customer active
• Backups encrypted and time-limited

✅ Integrity and confidentiality:
• Comprehensive security measures
• Regular security testing
• Employee training

text

### Legal Basis for Processing
📝 For Business Customers (Contract):
• Necessary for providing our services
• Outlined in Terms of Service and DPA

📝 For End Customers (Legitimate Interest):
• Businesses have legitimate interest in collecting reviews
• We process on behalf of businesses under DPAs
• SMS/email triggers require separate consent from businesses' customers

text

## Technical Implementation

### Data Protection by Design
🏗️ Architecture Features:
• Multi-tenant isolation via Row-Level Security
• Data encryption at application level
• No direct database access for customers
• API rate limiting and monitoring

🔐 Access Controls:
• Two-factor authentication for admin accounts
• Role-Based Access Control (RBAC)
• Principle of least privilege
• Session management and timeout

text

### Security Measures
🛡️ Infrastructure Security:
• Regular security patches and updates
• DDoS protection via Cloudflare
• Web Application Firewall (WAF)
• Regular vulnerability scanning

🔒 Data Security:
• AES-256 encryption for data at rest
• TLS 1.3 for data in transit
• Key management via HashiCorp Vault
• Regular security audits

text

### Incident Response
🚨 Response Plan:
• 24/7 monitoring and alerting
• Escalation procedures for breaches
• Customer notification within 72 hours if required
• Regulatory reporting procedures
• Post-incident review and improvement

text

## Data Processing Agreements (DPAs)

### Standard DPA Provisions
📑 Key Clauses:
• Processing instructions and purposes
• Security obligations
• Sub-processor notifications
• Data subject request handling
• Breach notification procedures
• Audit rights (with limitations)
• Data transfer mechanisms

🌍 International Transfers:
• Data primarily processed within EU/EEA
• Standard Contractual Clauses for any extra-EEA transfers
• Transparency about sub-processor locations

text

### Sub-processors
🤝 Current Sub-processors:
• Supabase (EU hosting, Sweden available)
• 46elks (Swedish SMS provider)
• Claude API (US, SCCs in place)
• DeepSeek API (depends on routing)
• Stripe (payment processing)

📋 Management:
• Sub-processor list maintained and updated
• Customers notified of changes
• DPAs with all sub-processors

text

## Data Subject Rights

### Right to Access
📋 For Business Customers:
• Access to their own data via dashboard
• Export functionality for their data
• Transparent data processing information

📋 For End Customers:
• Requests handled by business customers (Data Controllers)
• We provide tools for businesses to fulfill requests

text

### Right to Erasure (Right to be Forgotten)
🗑️ Implementation:
• Automated deletion upon customer request
• Cascading deletion across related data
• Backup purging procedures
• Anonymization option where deletion not possible

⏰ Timeline: Within 30 days of request

text

### Other Rights
🔍 Right to Rectification: Customers can update their information
🔄 Right to Portability: Data export in standard formats
⏸️ Right to Restriction: Temporary processing restrictions
🤖 Automated Decision-making: We don't make solely automated decisions with legal effect

text

## Data Retention Policies

### Retention Periods
📅 Business Customer Data:
• Active customers: Retained while account active
• Inactive customers: 30 days after cancellation, then anonymized
• Financial records: 7 years (legal requirement)

📅 End Customer Data (Reviews):
• Linked to business customer account
• Deleted when business customer deletes account or requests deletion
• Platform reviews cached for 30 days maximum

📅 Technical Data:
• Log files: 90 days
• Backups: 30 days, then permanently deleted
• Analytics: Anonymized after 14 months

text

### Deletion Procedures
🔄 Automated Deletion:
• Scheduled jobs for expired data
• Cascading deletion to maintain referential integrity
• Backup rotation and purging
• Verification of complete deletion

📝 Manual Deletion:
• Admin interface for customer data deletion
• Audit logging of all deletion actions
• Confirmation processes for bulk deletions

text

## International Considerations

### Data Transfers
🌍 Primary Data Location: EU/EEA
• Preference for Swedish data centers
• EU options for all sub-processors
• Clear documentation of data flows

🛡️ Extra-EEA Transfers:
• Only when necessary (e.g., AI APIs)
• Standard Contractual Clauses in place
• Additional safeguards where possible
• Transparency to customers

text

### Expansion Planning
🇳🇴 Norway/Denmark: Same EU/EEA framework applies
🇫🇮 Finland: EU member, similar compliance
🇩🇪 Germany: Stricter interpretations, planning required
🇬🇧 UK: Adequacy decision, similar requirements
🇺🇸 US: Requires additional safeguards, SCCs essential

text

## Cookies & Tracking

### Cookie Policy
🍪 Essential Cookies:
• Session management
• Security features
• No consent required

🍪 Analytics Cookies:
• Anonymized usage data
• Opt-out available
• Clear information provided

🍪 Marketing Cookies:
• Only with explicit consent
• Granular control options
• Easy withdrawal mechanism

text

### Tracking Technologies
📱 Our Use:
• Basic analytics for service improvement
• Error tracking for stability
• Performance monitoring
• All anonymized or pseudonymized

🎯 Third-party Tracking:
• Limited to essential services
• Documentation of all trackers
• Consent management for non-essential



## Vendor Management

### Due Diligence Process
🔍 Vendor Assessment:
• Security questionnaires
• Compliance documentation review
• Reference checks
• Ongoing monitoring

📋 Requirements for Vendors:
• GDPR compliance certification or evidence
• Security certifications (ISO 27001, SOC 2 preferred)
• Data breach notification procedures
• Right to audit clauses



### Contractual Protections
📝 Standard Clauses:
• Data protection obligations
• Security requirements
• Breach notification
• Audit rights
• Liability for vendor breaches



## Employee Training & Awareness

### Training Program
🎓 Initial Training:
• All employees complete GDPR training
• Role-specific data protection training
• Security awareness training

🔄 Ongoing Education:
• Annual refresher training
• Updates on regulatory changes
• Incident response drills
• Best practice sharing



### Policies & Procedures
📚 Documentation:
• Data Protection Policy
• Incident Response Plan
• Data Retention Policy
• Access Control Policy
• Vendor Management Policy



## Compliance Monitoring

### Regular Reviews
📅 Monthly:
• Access log reviews
• Security incident review
• Vendor compliance check

📅 Quarterly:
• Data protection impact assessments
• Policy and procedure review
• Training effectiveness assessment

📅 Annual:
• Comprehensive compliance audit
• Security penetration testing
• Regulatory change assessment


### Documentation
📁 Maintained Records:
• Data processing activities register
• Data protection impact assessments
• Security incident logs
• Training records
• Vendor assessments
• Consent records (where applicable)



## Breach Response Plan

### Detection & Assessment
🚨 Immediate Actions:
• Contain the breach
• Assess scope and impact
• Determine notification requirements
• Preserve evidence

⏰ Timeline:
• Initial assessment within 24 hours
• Regulatory notification within 72 hours if required
• Customer notification without undue delay



### Notification Procedures
📢 To Regulators:
• Swedish Authority for Privacy Protection (IMY)
• Required information as per GDPR Article 33
• Ongoing communication as investigation progresses

📢 To Affected Individuals:
• Clear, plain language explanation
• Description of likely consequences
• Measures taken or proposed
• Contact points for more information



## Future Compliance Planning

### Upcoming Regulations
🔮 ePrivacy Regulation: Monitoring development
🔮 AI Act: Planning for compliance when applicable
🔮 Digital Services Act: Reviewing implications
🔮 National Legislation: Tracking Swedish developments



### Continuous Improvement
🔄 Process:
• Regular gap analysis against best practices
• Customer feedback incorporation
• Industry standard adoption
• Proactive rather than reactive approach



## Customer Resources

### Provided to Business Customers
📋 Template Documents:
• Privacy policy template
• Consent language suggestions
• Data subject request handling guide
• Breach notification checklist

🔧 Technical Tools:
• Data export functionality
• User deletion tools
• Consent management features
• Audit logging access



### Support & Guidance
🤝 Customer Support:
• GDPR questions answered
• Best practice guidance
• Configuration assistance
• Regular compliance updates



---

## Contact Information

### Data Protection Contact
👤 Responsible Person: Pierre Camilo (Founder & CEO)
📧 Email: privacy@reputera.se
📍 Address: Östgötagatan 91
🌐 Website: https://reputera.se/integritetspolicy/

🇸🇪 Swedish Supervisory Authority:
Integritetsskyddsmyndigheten (IMY)
Box 8114, 104 20 Stockholm
www.imy.se



### Reporting Concerns
📢 Security Vulnerabilities: security@reputera.se
📢 Privacy Concerns: privacy@reputera.se
📢 General Inquiries: support@reputera.se

⏰ Response Time: We aim to respond within 48 hours



---

*This document is reviewed quarterly and updated as needed. Last updated: March 2024. We are committed to maintaining the highest standards of data protection and privacy for all our users.*
