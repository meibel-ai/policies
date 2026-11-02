# Security overview

**Effective 2 November 2026**

- **Independent audit:** Meibel's controls are examined each year in a SOC 2 Type II audit against the
  Security criteria. Customers can request the current report, and a bridge letter covering the time since
  it ended, under a confidentiality agreement.
- **Encryption:** customer data is encrypted in transit (TLS 1.2 or higher) and at rest, and connections to
  production systems use encrypted protocols.
- **Separation:** network segmentation isolates parts of the production environment, and each customer's
  data is logically separated from other customers'.
- **Access control:** access to production follows least privilege, requires multi-factor authentication,
  is reviewed regularly, and is removed promptly when no longer needed.
- **Logging and monitoring:** security-relevant activity in production systems is logged, monitored and
  alerted on.
- **Vulnerability management:** internal and external vulnerability scans run at least quarterly, and
  findings are fixed within timeframes set by severity. Production systems are immutable: they are replaced
  rather than patched in place.
- **Resilience:** production runs across multiple availability zones with automatic failover. Production
  data is backed up, restoring from backup is tested at least once a year, and business continuity and
  disaster recovery plans are tested at least once a year.
- **People:** staff pass background checks where the law allows, sign confidentiality agreements, and
  complete security awareness training at least once a year.
- **Vendors:** Meibel keeps a register of its vendors and reviews critical vendors before relying on them.
- **Incidents and risk:** Meibel maintains a documented incident response plan and assesses security risk
  at least once a year.
