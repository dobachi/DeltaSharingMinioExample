# DeltaSharingMinioExample

## Configurations

There are examples of configuration files under `conf` directory.

* delta-sharing-minio.yaml
  * Configuration for Delta Sharing Server
* core-site.xml
  * Configuration for Delta Sharing Server about Apache Hadoop
* minio.share
  * Configuration for Delta Sharing client

## Preparements

### Start MinIO


You can download executable packages from the official web site [MinIO] .

[MinIO]: https://min.io/

Start MinIO process.

```shell
$ mkdir -p ~/MinIO
$ cd ~/MinIO
$ wget https://dl.min.io/server/minio/release/linux-amd64/minio
$ chmod +x minio
$ ./minio server ./data
```

You can also use `mc` command to control your MinIO.

### Create sample data

You can create dummy data with the notebook.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/CreateDummyDataOnMinIO.ipynb

There is a helper script to start Jupyter with PySpark.

```
$ ./bin/jupyterlab.sh
```

## Using Delta Sharing to read data

### Start Delta Sharing

Start [Delta Sharing]

Use the following configuration.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/core-site.xml

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/delta-sharing_minio.yaml

[Delta Sharing]: https://delta.io/sharing/

```shell
$ ./bin/delta-sharing-server -- --conf conf/delta-sharing-server_minio.yaml
```

### Load data via Delta Sharing

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/LoadDataViaDeltaSharing.ipynb

Use the following configuration in the notebook.

https://github.com/dobachi/DeltaSharingMinioExample/blob/main/conf/minio.share
