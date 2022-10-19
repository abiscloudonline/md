## Amazon RDS:
Collection of managed services that makes it simple to set up, operate, and scale databases in the cloud.
## What is Multi-AZ:
 * In Multi-AZ deployment, Amazon RDS automatically creates a primary database (DB) instance and synchronously replicates the data to an
instance in a different availability zone.
 * When it detects a failure, Amazon RDS automatically fails over to a standby instance without manual intervention.
## Read Replica:
 * The read replica operates as a DB instance that allows only read-only connections;
 * Applications can connect to a read replica just as they would to any DB instance.
 * Amazon RDS replicates all databases in the source DB instance.
## Disaster Recovery:
## Advantages of DR in cloud over traditional environments:
* Recover quickly from a disaster with reduced complexity
* Simple and repeatable testing allow you to test more easily and more frequently
* Lower management overhead decreases operational burden
* Opportunities to automate decrease chances of error and improve recovery time
## Disaster recovery of RDS
* Amazon RDS creates and saves automated backups of your DB instance during the backup window of your DB instance. 
* Creates a storage volume snapshot of your DB instance, backing up the entire DB instance and not just individual databases
## Automated backups follow these rules:
* DB instance must be in the AVAILABLE state for automated backups to occur. 
* Automated backups don't occur while your DB instance is in a state other than AVAILABLE, for example STORAGE_FULL.
* Automated backups don't occur while a DB snapshot copy is running in the same AWS Region for the same DB instance.
## DB Snapshots:
* The first snapshot of a DB instance contains the data for the full DB instance. 
* Subsequent snapshots of the same DB instance are incremental, which means that only the data that has changed after your most recent snapshot is saved
## Cross Region Backups:
* For added disaster recovery capability, you can configure your Amazon RDS database instance to replicate snapshots and transaction logs to a destination AWS Region of your choice. 
* When backup replication is configured for a DB instance, RDS initiates a cross-Region copy of all snapshots and transaction logs as soon as they are ready on the DB instance.
## I/O activity:
 * Creating this DB snapshot on a Single-AZ DB instance results in a brief I/O suspension that can last from a few seconds to a few minutes.
 * For PostgreSQL, I/O activity is not suspended on your primary during backup for Multi-AZ deployments, because the backup is taken from the standby.
## Exporting DB snapshot data to Amazon S3
* You can export DB snapshot data to an Amazon S3 bucket. 
* The export process runs in the background and doesn't affect the performance of your active DB instance.
* When you export a DB snapshot, Amazon RDS extracts data from the snapshot and stores it in an Amazon S3 bucket.
* The data is stored in an Apache Parquet format that is compressed and consistent.
![image](https://user-images.githubusercontent.com/107330427/196696907-f598c37a-1a7a-4392-b7c9-f618581804d8.png)
