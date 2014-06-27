# Visualforce + AngularJS + Bootstrap

A simple project that creates a Visualforce page that contains AngularJS and Bootstrap.

To create the page in Salesforce, add the following to a new file named `gradle.properties` in this directory:

    forceUsername=foo@bar.com
    forcePassword=passwordandsecuritytoken

Deploy the page:

    ./gradlew forceMetadataDeploy
