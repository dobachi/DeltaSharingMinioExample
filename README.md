# DeltaSharingMinioExample

## Configurations

* delta-sharing-minio.yaml
  * Configuration for Delta Sharing Server
* core-site.xml
  * Configuration for Delta Sharing Server about Hadoop
* minio.share
  * Configuration for Delta Sharing client

## Preparements

### Start MinIO

Start [MinIO]

### Create sample data

You can create dummy data with the notebook.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/CreateDummyDataOnMinIO.ipynb

### Start Delta Sharing

Start [Delta Sharing]

Use the following configuration.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/core-site.xml

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/delta-sharing-minio.yaml

[Delta Sharing]: https://delta.io/sharing/

### Load data via Delta Sharing

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/LoadDataViaDeltaSharing.ipynb

Use the following configuration in the notebook.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/minio.share

[MinIO]: https://min.io/
