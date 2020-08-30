# NICE Attendance Taker
![Logo](/images/NICE-icon.png)

NICE (NFC-Integrated Cards for Entry) attendance management system.

[![Build Status](https://travis-ci.com/sudiamanj/NICE.svg?branch=master)](https://travis-ci.com/sudiamanj/NICE)

## Setup

### Requirements
- [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html) (8u40 or later)
- [Apache Maven](https://maven.apache.org/)
- [MySQL](https://www.mysql.com/)
- [ACR122U USB NFC Reader](https://www.acs.com.hk/en/products/3/acr122u-usb-nfc-reader)

### Steps
- Connect your ACR122U USB NFC Reader. The device should be showing a red light. If not, ensure that you have the correct drivers installed. On Windows, you may need to start the “Smart Card” service as well.
- In MySQL, create a database named `nicedb`. Initialize it using [DDL.sql](/src/main/resources/com/sudicode/nice/DDL.sql).
- Set the following environment variables:

| Variable    | Value                                       |
|-------------|---------------------------------------------|
| `DB_USER`   | Your database username, e.g. `root`         |
| `DB_PW`     | Your database password                      |
| `DB_SERVER` | Location of your database, e.g. `localhost` |

- Start NICE using the following command:

```shell
mvn install && mvn exec:java
```

## See it in action!
<a href="https://vimeo.com/228209879"><img src="/images/demo.png" alt="Video Demo"></a>
