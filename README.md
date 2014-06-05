s3-ganglia-scripts
==================

An updated version of Amazon's Ganglia install scripts to use Ganglia 3.6.0

Usage
=====

To use these scripts, they need to be configured to use your S3 bucket.
In ganglia-installer, you need to replace `###BUCKET_NAME###` with your bucket name.
Then you need to upload them into the root directory of your bucket, along with ganglia-3.6.0.tar.gz and ganglia-web-3.5.10.tar.gz available from: [http://ganglia.info/?page_id=66](http://ganglia.info/?page_id=66)

When running your EMR job, you have to specify install-ganglia as a bootstrap action. eg
`--bootstrap-action s3://###BUCKET_NAME###/install-ganglia`
