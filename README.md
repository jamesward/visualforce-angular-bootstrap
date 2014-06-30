# Visualforce + AngularJS + Bootstrap

A simple project that creates a Visualforce page that contains AngularJS and Bootstrap.

To create the page in Salesforce, add the following to a new file named `gradle.properties` in this directory:

    forceUsername=foo@bar.com
    forcePassword=passwordandsecuritytoken

Deploy the page:

    ./gradlew forceMetadataDeploy

To enable the new page to show up in the Salesforce1 mobile app, visit the [Mobile Navigation](https://login.salesforce.com/?ec=302&startURL=%2Fsetup%2Fsalesforce1AppMenu.apexp) page in Setup, add the new *Hello* page, and select *Save*.
