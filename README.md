SDIA Demo

ShadowNode Domain Intelligence Analyzer — Public Demo

A simple early-access interface for testing ShadowNode Domain Intelligence Analyzer (SDIA), the domain intelligence engine behind ShadowNode.

SDIA analyzes publicly observable domain infrastructure and produces structured intelligence that can support OSINT, security research, threat intelligence, and digital investigations.

🌐 Try SDIA

The public demo is available here:

https://sdia.shadownodebureau.com

Enter a domain such as:

example.com

and select Analyze.

The demo displays investigation metrics and the structured response returned by the SDIA API.

---

What It Can Analyze

SDIA currently provides intelligence across several areas:

- Domain registration / RDAP
- DNS records
- IPv4 and IPv6 resolution
- ASN and network observations
- HTTP response information
- HTTP security headers
- TLS and certificate information
- Certificate Transparency
- CT hostname observations
- Infrastructure relationships
- Shared infrastructure correlations
- Findings
- Evidence artifacts
- Evidence provenance and integrity information

The goal is not simply to collect information.

SDIA is designed to help move an investigation through:

Observation
     ↓
Normalization
     ↓
Correlation
     ↓
Finding
     ↓
Evidence
     ↓
Verification

Observed information and analytical conclusions are intentionally kept distinguishable.

---

Evidence-Preserving Intelligence

SDIA is designed around the principle:

«Observed evidence should remain distinguishable from analytical conclusions.»

Collection results can be represented as structured evidence artifacts containing information such as:

- Artifact identifiers
- Collection sources
- Collection timestamps
- Collector information
- Evidence classification
- Parent artifact references
- SHA-256 integrity hashes

Derived relationships can maintain references to the observations from which they were produced.

This allows findings to be traced back to their supporting evidence.

---

Infrastructure Correlation

SDIA can identify relationships between publicly observable infrastructure, including:

- Shared IP addresses
- Shared ASNs
- DNS observations
- Certificate-associated hostnames
- CT-to-DNS relationships

Correlations should be interpreted carefully.

For example, multiple domains resolving to the same IP address indicate shared observed infrastructure.

That does not, by itself, prove:

- Common ownership
- Common administrative control
- Common application ownership
- Organizational affiliation
- Intentional association

Similarly, Certificate Transparency observations do not automatically prove that a hostname is currently active.

SDIA therefore separates current observations from historical or certificate-associated observations.

---

Architecture

                 Public SDIA Demo
                        |
                        v
                    SDIA API
                        |
                        v
                 Private SDIA Engine
                        |
          +-------------+-------------+
          |             |             |
          v             v             v
       Collection   Correlation    Evidence
          |             |             |
          +-------------+-------------+
                        |
                        v
                    Findings
                        |
                        v
                   Verification

The public repository contains the demo interface only.

The SDIA intelligence engine and its underlying implementation are maintained separately and are not included in this repository.

---

Public Demo Architecture

GitHub Pages Demo
        |
        v
     SDIA API
        |
        v
 Private SDIA Engine
        |
        +-- Domain Intelligence
        +-- Infrastructure Correlation
        +-- Findings
        +-- Evidence
        +-- Verification

The public interface is intentionally separated from the private intelligence engine.

This allows the underlying collection and intelligence pipeline to evolve independently from the public demonstration interface.

---

Early Access

SDIA v0.1.0 is currently available as an early-access release.

The public demo is intentionally minimal.

The current focus is to validate the intelligence capability, investigation workflow, evidence model, and usefulness of the resulting observations before expanding the public interface.

Try it

Visit:

https://sdia.shadownodebureau.com

Try different domains and explore the resulting intelligence.

---

Feedback

Feedback is actively welcomed.

If you test SDIA, useful feedback includes:

- What intelligence was most useful?
- What observations were missing?
- Which correlations would help your investigations?
- What findings would you like to see?
- What would improve the investigation workflow?
- Were any results difficult to interpret?
- What would make SDIA more useful for professional investigations?

Don't just tell us that it works.

Tell us what would make it better.

---

Responsible Use

SDIA is intended for legitimate:

- Security research
- OSINT
- Defensive security
- Threat intelligence
- Digital investigations
- Infrastructure analysis
- Authorized security work

Only analyze domains and infrastructure where you have an appropriate legal or operational basis to do so.

Users are responsible for complying with applicable laws, organizational policies, service terms, privacy requirements, and authorization boundaries.

SDIA is designed around publicly observable information. This does not remove the responsibility to use collected information appropriately.

---

Limitations

SDIA is an observation and correlation tool.

It does not guarantee:

- Ownership attribution
- Identity attribution
- Infrastructure ownership
- Historical completeness
- Current availability of every discovered hostname
- Definitive relationships between correlated systems
- Legal admissibility of generated evidence

Network infrastructure changes over time. DNS, IP, ASN, HTTP, TLS, and other observations represent the state observed during a particular collection.

External data sources may also change their responses, availability, rate limits, and coverage.

---

Status

SDIA v0.1.0 — Early Access

The current release focuses on the core:

Passive Collection
       +
Normalization
       +
Infrastructure Correlation
       +
Evidence Preservation
       +
Finding Provenance
       +
Verification

The public interface will evolve as testing and feedback continue.

---

Feedback and Contributions

Researchers, investigators, OSINT practitioners, cybersecurity professionals, and other authorized users are encouraged to test the demo and provide feedback.

Particularly valuable areas include:

- Domain intelligence
- Infrastructure relationships
- Investigation workflow
- Evidence presentation
- Correlation quality
- Usability
- Missing intelligence sources

---

ShadowNode Operations Bureau

ShadowNode Domain Intelligence Analyzer

Intelligence. Investigation. Evidence.