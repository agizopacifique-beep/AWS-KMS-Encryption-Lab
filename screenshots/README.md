Screenshots and Evidence
#	Category	File Name	Security Validation
01	KMS Setup	kms-key-created.png	Customer managed key created and ready for encryption use
02	S3 Encryption	s3-bucket-encryption.png	Default SSE KMS encryption configured on bucket
03	S3 Encryption	encrypted-upload.png	Object uploaded with KMS encryption enabled
04	S3 Validation	object-encryption-confirmed.png	Object metadata confirms encryption applied
05	Access Control	public-access-denied.png	Public access blocked, no unauthorized exposure
06	Access Control	invalid-argument-error.png	Invalid access attempt rejected by S3
07	Access Control	signed-access-success.png	Secure access works with authenticated request
08	Monitoring	cloudtrail-kms-filter.png	CloudTrail shows visibility into KMS operations
09	Monitoring	generate-data-key-event.png	GenerateDataKey event confirms encryption workflow
10	Monitoring	decrypt-event.png	Decrypt event confirms secure data access
11	EBS Baseline	unencrypted-volume.png	Initial state shows unencrypted root volume
12	EBS Migration	snapshot-created.png	Snapshot created for encryption process
13	EBS Migration	encrypted-volume-created.png	New encrypted volume created using KMS
14	EBS Migration	volumes-labeled.png	Clear distinction between volumes
15	EBS Migration	volume-swapped.png	Encrypted volume successfully attached
16	Failure Test	key-disabled.png	KMS key disabled to simulate outage
17	Failure Test	instance-failed-to-start.png	EC2 fails to boot without key access
18	Failure Test	s3-kms-disabled-error.png	S3 access fails due to disabled key
19	Monitoring	cloudtrail-disable-event.png	CloudTrail logs key disable event
20	Recovery	key-re-enabled-instance-running.png	Services restored after key activation
21	Validation	lab-score.png	Lab completion and verification
