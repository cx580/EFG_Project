# EFG_Project

The centrol logging solution based on graylog, elastic search and filebeat。

### Architecture

![logo](https://github.com/cx580/EFG_Project/blob/master/pic/architecture.png)

### Log Spec

The log is formatted with `JSON`.

The log contains tree parts:

- Log common header part, defined in company level. Normally, this part is defined in logback/log4j config, it is not need to be set by application,
- Log service header part, it is defined by service owner, and need to be set by application developer in code
- Log body part

#### Log common header part

- Timestamp
- Threadid
- Log Level 
- Host IP
- Domain Name
- Service Name

#### Log service header part

- Component Name
- Traceid (From APM, optional)
- Other headers, for example: userid, orderid..





