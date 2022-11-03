## Connecto to mongo via command line

> Instancia Pancho Pepe

```bash
mongo -u ibm_cloud_50efede8_1ed6_4af9_bdd7_4781fce5df4b -p 7ef8bc79d5bbbf186aa7b4d200b4682177bfeb8d391c7bea136b7d72b4a8d5fb --ssl --ssCAFile cert.pem --authenticationDatabase admin --host replset/afbce620-2768-4f16-be4c-ee88f7b2ba81-0.8f7bfd8f3faa4218aec56e069eb46187.databases.appdomain.cloud:32675,afbce620-2768-4f16-be4c-ee88f7b2ba81-1.8f7bfd8f3faa4218aec56e069eb46187.databases.appdomain.cloud:32675
```

> Instancia Innovgro

`mongodb://ibm_cloud_302623d6_61ec_4539_8a07_6397bfbb77dc:d2b2f091a0fe701bf4e3c452c939e4d9b4a25608d8aef9bbb9d27d13aada46e7@bec06f3c-5f0a-437b-856b-333b1d203853-0.66c11f9786bc40cfa3a0086f6582f2e7.databases.appdomain.cloud:31230,bec06f3c-5f0a-437b-856b-333b1d203853-1.66c11f9786bc40cfa3a0086f6582f2e7.databases.appdomain.cloud:31230/ibmclouddb?authSource=admin&replicaSet=replset`

## Comando para hacer dump (Export)

mongodump --host replset/afbce620-2768-4f16-be4c-ee88f7b2ba81-0.8f7bfd8f3faa4218aec56e069eb46187.databases.appdomain.cloud:32675,afbce620-2768-4f16-be4c-ee88f7b2ba81-1.8f7bfd8f3faa4218aec56e069eb46187.databases.appdomain.cloud:32675 -d ibmclouddb -u ibm_cloud_50efede8_1ed6_4af9_bdd7_4781fce5df4b -p 7ef8bc79d5bbbf186aa7b4d200b4682177bfeb8d391c7bea136b7d72b4a8d5fb --ssl --sslCAFile cert.pem --authenticationDatabase admin -o /Users/matisalimba/dev/office-mobile/backup

## Comando para hacer restore (Import)

mongorestore --host replset/bec06f3c-5f0a-437b-856b-333b1d203853-0.66c11f9786bc40cfa3a0086f6582f2e7.databases.appdomain.cloud:31230,bec06f3c-5f0a-437b-856b-333b1d203853-1.66c11f9786bc40cfa3a0086f6582f2e7.databases.appdomain.cloud:31230 -d mobileoffice -u ibm_cloud_302623d6_61ec_4539_8a07_6397bfbb77dc -p d2b2f091a0fe701bf4e3c452c939e4d9b4a25608d8aef9bbb9d27d13aada46e7 --ssl --sslCAFile cert2.pem --authenticationDatabase admin /Users/matisalimba/dev/office-mobile/backup/ibmclouddb

##

> blue-green https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html

##
# mobile-office
