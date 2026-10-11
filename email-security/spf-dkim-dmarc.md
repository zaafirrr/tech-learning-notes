
# 🔐 SPF, DKIM & DMARC

A quick introduction to three email authentication mechanisms that help protect domains against spoofing and phishing.

## 📖 What Are They?

### 1. SPF — Sender Policy Framework

SPF specifies which mail servers are authorised to send emails on behalf of a domain.

**Key takeaway:** Helps receiving servers check whether the sending server is authorised for the relevant envelope sender domain.

### 2. DKIM — DomainKeys Identified Mail

DKIM uses a cryptographic signature to help receiving servers verify that signed parts of an email have not been altered.

**Key takeaway:** Provides a way to verify an email's signature and its association with a signing domain.

### 3. DMARC — Domain-based Message Authentication, Reporting and Conformance

DMARC builds on SPF and DKIM. It checks whether at least one authentication mechanism passes and aligns with the domain in the email's visible `From` address.

**Key takeaway:** Allows domain owners to publish policies for handling messages that fail DMARC and receive reports about authentication results.

---

## 📊 Quick Comparison

| Mechanism | What It Checks | Main Benefit |
|---|---|---|
| **SPF** | Authorised sending servers | Sender authorisation |
| **DKIM** | Cryptographic email signature | Message integrity and domain authentication |
| **DMARC** | SPF/DKIM results and domain alignment | Policy enforcement and reporting |

## 🔄 How They Work Together

1. **SPF** checks whether a sending server is authorised for its envelope sender domain.
2. **DKIM** verifies the email's cryptographic signature.
3. **DMARC** evaluates whether SPF or DKIM passes and aligns with the visible `From` domain.

An email can pass SPF or DKIM and still fail DMARC if the required alignment is missing.

## 🛡️ Why Does It Matter?

- Helps reduce domain spoofing.
- Supports protection against phishing and impersonation.
- Gives domain owners visibility into authentication failures.
- Helps organisations enforce email authentication policies.

*Email authentication is an important security layer, but it does not prevent every phishing attack.*

## 📚 Further Reading

- [SPF — Microsoft Learn](https://learn.microsoft.com/en-us/defender-office-365/email-authentication-spf-configure)
- [DKIM — Microsoft Learn](https://learn.microsoft.com/en-us/defender-office-365/email-authentication-dkim-configure)
- [DMARC — Microsoft Learn](https://learn.microsoft.com/en-us/defender-office-365/email-authentication-dmarc-configure)

---
