# AWS KMS Encryption Lab

A hands-on AWS security lab demonstrating end-to-end encryption using AWS Key Management Service (KMS) across S3, EC2, and EBS — including access control enforcement, CloudTrail audit logging, EBS volume migration, and a full failure/recovery simulation.

---

## Overview

| Detail | Value |
|---|---|
| Key Type | Customer Managed Key (CMK) |
| Services Used | AWS KMS, Amazon S3, Amazon EC2, Amazon EBS, AWS CloudTrail |
| Encryption Method | SSE-KMS |
| Failure Tested | Yes |
| Screenshots | 21 |

---

## Lab Phases

### Phase 1 — KMS Setup

| # | Screenshot | Description |
|---|---|---|
| 01 | `kms-key-created.png` | Customer managed key created and ready for encryption use |

---

### Phase 2 — S3 Encryption

| # | Screenshot | Description |
|---|---|---|
| 02 | `s3-bucket-encryption.png` | Default SSE-KMS encryption configured on the bucket |
| 03 | `encrypted-upload.png` | Object uploaded with KMS encryption enabled |
| 04 | `object-encryption-confirmed.png` | Object metadata confirms encryption was applied |

---

### Phase 3 — Access Control

| # | Screenshot | Description |
|---|---|---|
| 05 | `public-access-denied.png` | Public access blocked — no unauthorized exposure |
| 06 | `invalid-argument-error.png` | Invalid access attempt rejected by S3 |
| 07 | `signed-access-success.png` | Secure access confirmed with authenticated pre-signed request |

---

### Phase 4 — CloudTrail Monitoring

| # | Screenshot | Description |
|---|---|---|
| 08 | `cloudtrail-kms-filter.png` | CloudTrail filter applied to surface KMS operations |
| 09 | `generate-data-key-event.png` | GenerateDataKey event confirms encryption workflow |
| 10 | `decrypt-event.png` | Decrypt event confirms secure data access |

---

### Phase 5 — EBS Encryption Migration

| # | Screenshot | Description |
|---|---|---|
| 11 | `unencrypted-volume.png` | Initial state — unencrypted root volume baseline |
| 12 | `snapshot-created.png` | Snapshot created to begin the encryption migration |
| 13 | `encrypted-volume-created.png` | New encrypted volume created from snapshot using KMS |
| 14 | `volumes-labeled.png` | Clear distinction between old and new volumes |
| 15 | `volume-swapped.png` | Encrypted volume successfully attached to the instance |

---

### Phase 6 — Failure Simulation

| # | Screenshot | Description |
|---|---|---|
| 16 | `key-disabled.png` | KMS key disabled to simulate a service outage |
| 17 | `instance-failed-to-start.png` | EC2 instance fails to boot without key access |
| 18 | `s3-kms-disabled-error.png` | S3 access fails due to the disabled KMS key |
| 19 | `cloudtrail-disable-event.png` | CloudTrail logs the key disable event for audit |

---

### Phase 7 — Recovery and Validation

| # | Screenshot | Description |
|---|---|---|
| 20 | `key-re-enabled-instance-running.png` | All services restored after key re-activation |
| 21 | `lab-score.png` | Lab completion and final verification score |

---

## Key Concepts Demonstrated

- Creating and managing a Customer Managed Key (CMK) in AWS KMS
- Enforcing default SSE-KMS encryption on an S3 bucket
- Blocking public access and validating pre-signed URL authentication
- Auditing KMS operations (GenerateDataKey, Decrypt) via CloudTrail
- Migrating an unencrypted EBS volume to an encrypted one using snapshots
- Simulating key-level failure and observing downstream impact on EC2 and S3
- Restoring services by re-enabling a disabled KMS key
