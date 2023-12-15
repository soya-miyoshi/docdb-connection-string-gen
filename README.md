# docdb-connection-string-gen
Generate Docdb connection String from CNAME for DocumentDB Cluster and Secret Manager Secret ARN.  
This script downloads globa-bundle.pem under the current directory.  

# prerequisite
The URL pointing to your AWS DocumentDB cluster must be registered with a CNAME record.  

# Usage
`./global-bundle.pem` is installed by this script if it does not exit and the port is assumed to be 27017
```
$ ./generate-connection-url.sh <CNAME> <SECRET_ARN>
mongodb://username:password@host:27017/?tls=true&tlsCAFile=./global-bundle.pem
```
