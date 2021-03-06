PDex Patient Import UI Reference Implementation
===============
[![Build Status](https://travis-ci.org/HL7-DaVinci/PDex-Patient-Import-UI.svg?branch=master)](https://travis-ci.org/github/HL7-DaVinci/PDex-Patient-Import-UI)

Da Vinci reference implementation for the Patient Import UI use case.

# Implementation Details
Implementation is intended to prove the following functionality:
1. OAuth2 Authorization for data import from multiple Payer systems.
2. Querying of Patient data from a Payer FHIR Server using a token requested during step 1
3. Storing Patient data from multiple Payer systems.
4. Responsive UI to display Patient data.
5. Group data by Encounter.

# Build
This project is dependent on a module from https://github.com/HL7-DaVinci/PDex-Patient-Import-App Reference Implementation. Check out sources and run the following command from root:
```sh
./gradlew clean build publishToMavenLocal
```
This will publish all required dependencies to your local Maven repository and make them avialable for this project. Do this step only when something has changed in Patient Import App RI.
After that go to PDex Patient Import UI project and run:
```sh
mvn clean install
```

# Try it
Run app with
```sh
java -jar target/patient-ui-1.0-SNAPSHOT.jar
```
Go to http://localhost:8080

Credentials: user/user
