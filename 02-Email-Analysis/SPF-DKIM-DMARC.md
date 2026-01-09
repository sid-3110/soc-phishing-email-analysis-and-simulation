# SPF, DKIM, and DMARC Analysis

## Objective
To validate the presence and enforcement of email authentication mechanisms using industry-standard tools.

## Tools Used
- Google Admin Toolbox (Messageheader)
- MXToolbox / PowerDMARC / dmarcian (DNS validation)

---

## SPF (Sender Policy Framework)
**Result:** Not present

**Explanation:**
No SPF record was found authorizing the sending server to send emails on behalf of the domain.

**SOC Interpretation:**
Lack of SPF allows unauthorized servers to send spoofed emails using the domain.

---

## DKIM (DomainKeys Identified Mail)
**Result:** Not present

**Explanation:**
The email did not contain a DKIM signature to verify message integrity.

**SOC Interpretation:**
Without DKIM, the email content cannot be cryptographically validated.

---

## DMARC (Domain-based Message Authentication, Reporting & Conformance)
**Result:** Not enforced

**Explanation:**
No DMARC policy was defined to instruct receiving servers how to handle authentication failures.

**SOC Interpretation:**
Absence of DMARC significantly weakens email security posture.

---

## Combined SOC Assessment
While authentication failures alone do not confirm phishing, the absence of SPF, DKIM, and DMARC combined with social engineering indicators increases phishing confidence.

**Final Assessment:** Suspicious

<img width="1888" height="867" alt="Screenshot 2026-01-09 211130" src="https://github.com/user-attachments/assets/e1dcbb83-5b99-438b-b96b-1235f51b8871" />


