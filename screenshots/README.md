# Screenshots

All screenshots captured during AWS KMS Encryption Lab 5.1.
Each file is numbered and named to match its task.

| File | What It Shows |
|------|--------------|
| `01-kms-key-created.png` | MyKMSKey created in KMS console |
| `02-s3-bucket-encryption.png` | Default encryption settings on ImageBucket |
| `03-encrypted-upload.png` | SSE-KMS configuration when uploading clock.png |
| `04-object-encryption-confirmed.png` | clock.png properties confirming SSE-KMS |
| `05-public-access-denied.png` | Access Denied via public S3 URL |
| `06-invalid-argument-error.png` | Invalid Argument error after making object public |
| `07-signed-access-success.png` | clock.png loaded via signed URL |
| `08-cloudtrail-kms-filter.png` | CloudTrail filtered to KMS events |
| `09-generate-data-key-event.png` | GenerateDataKey event from S3 upload |
| `10-decrypt-event.png` | Decrypt event from opening the S3 object |
| `11-unencrypted-volume.png` | LabInstance showing unencrypted root volume |
| `12-snapshot-created.png` | Unencrypted Root Volume snapshot |
| `13-encrypted-volume-created.png` | New encrypted volume from snapshot |
| `14-volumes-labeled.png` | Both volumes labeled in EBS console |
| `15-volume-swapped.png` | Encrypted volume attached to LabInstance |
| `16-key-disabled.png` | MyKMSKey disabled in KMS console |
| `17-instance-failed-to-start.png` | LabInstance failing to start |
| `18-s3-kms-disabled-error.png` | KMS DisabledException on S3 object |
| `19-cloudtrail-disable-event.png` | DisableKey event in CloudTrail |
| `20-key-re-enabled-instance-running.png` | Key re-enabled and instance running |
| `21-lab-score.png` | Final submission report and score |
