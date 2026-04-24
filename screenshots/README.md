# Screenshots

Screenshots and Evidence

All screenshots document validation of encryption, access control, logging, and failure impact.

File	Evidence
01-kms-key-created.png	Customer managed KMS key successfully created and available for encryption operations
02-s3-bucket-encryption.png	Default bucket encryption configured using SSE KMS
03-encrypted-upload.png	S3 object uploaded with KMS encryption enabled
04-object-encryption-confirmed.png	Object metadata confirms SSE KMS encryption applied
05-public-access-denied.png	Public access blocked, confirms no unauthorized plaintext exposure
06-invalid-argument-error.png	Misconfigured public access attempt fails, validates enforcement of encryption requirements
07-signed-access-success.png	Controlled access works using authenticated request
08-cloudtrail-kms-filter.png	CloudTrail filtering shows visibility into KMS activity
09-generate-data-key-event.png	KMS GenerateDataKey event confirms envelope encryption workflow
10-decrypt-event.png	KMS Decrypt event confirms secure access to encrypted object
11-unencrypted-volume.png	Baseline EC2 root volume without encryption
12-snapshot-created.png	Snapshot used as migration step toward encryption
13-encrypted-volume-created.png	Encrypted EBS volume created using KMS key
14-volumes-labeled.png	Clear identification of encrypted versus unencrypted volumes
15-volume-swapped.png	Successful replacement of root volume with encrypted version
16-key-disabled.png	KMS key disabled to simulate security failure scenario
17-instance-failed-to-start.png	EC2 boot failure proves dependency on KMS key
18-s3-kms-disabled-error.png	S3 access failure confirms encryption enforcement when key is unavailable
19-cloudtrail-disable-event.png	CloudTrail logs key disable action for audit tracking
20-key-re-enabled-instance-running.png	Service restored after key reactivation
21-lab-score.png	Lab completion and validation of all required tasks
