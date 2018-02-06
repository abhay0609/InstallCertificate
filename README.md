# InstallCertificate


Usage:

### Need to compile, first:
```
javac InstallCert.java
```



### Access server, and retrieve certificate (accept default certificate 1)
java InstallCert [host]

### Extract certificate from created jssecacerts keystore
```
keytool -exportcert -alias [host]-1 -keystore jssecacerts -storepass changeit -file [host].cer
```


### Import certificate into system keystore
```
keytool -importcert -alias [host] -keystore [path to system keystore] -storepass changeit -file [host].cer
```


