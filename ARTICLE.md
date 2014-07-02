Building Salesforce1 Apps with Visualforce, AngularJS, and Bootstrap
--------------------------------------------------------------------

Modern web applications shift the user interface (UI) logic from the server-side to the client-side to reduce interaction latency and avoid unnecessary server requests.  This is done by running the UI logic in JavaScript.  Numerous JavaScript libraries exist to help developers organize their logic and create a maintainable separation of concerns.  There also now exists numerous CSS libraries that make it easy to build a good looking UI.

One of the most popular modern JavaScript UI libraries is AngularJS since it supports data binding and makes it easy to separate the Model, View, and Controller (MVC) aspects of the UI.  For styling the UI, Bootstrap is the most popular CSS library.

Both AngularJS and Bootstrap are easy to use in Visualforce pages that work both on desktop browsers and in the Salesforce1 mobile app.  Here is a quick video walkthrough that shows how to get started:
https://www.youtube.com/watch?v=Q1XyZlzt4N8

Here is the Visualforce code:
```
<apex:page docType="html-5.0">

    <apex:stylesheet value="//cdn.jsdelivr.net/webjars/bootstrap-sf1/0.1.0-beta.6/css/bootstrap-namespaced.css"/>
    
    <apex:includeScript value="//ajax.googleapis.com/ajax/libs/angularjs/1.3.0-beta.11/angular.min.js"/>
    
    <script>
        angular.module("ngApp", []);
    </script>
        
    <div class="bootstrap" ng-app="ngApp">
        <form>
            <label>Name:</label>
            <input type="text" ng-model="yourName" placeholder="Enter a name here"/>
            <hr/>
            <h1>Hello {{yourName}}!</h1>
        </form>
    </div>
    
</apex:page>
```

Make sure you enable the Available for Salesforce mobile apps option when creating the Visualforce page so that it can be made available in the Salesforce1 app.  After creating the page you can create a new tab in Salesforce by going to Setup > Create > Tabs and selecting New in the Visualforce Tabs section.  To enable the new tab to show up in the Salesforce1 app go to Setup > Mobile Administration > Mobile Navigation and then add the new tab to the selected list and save it.

This is a very simple example so everything is just in one page.  As an application grows the different pieces of the JavaScript application can be separated out into different files using Static Resources.  The AngularJS and Bootstrap libraries could also be uploaded as Static Resource if you’d rather not use the public CDNs.

The Bootstrap CSS in this example uses the Salesforce1 themed version of Bootstrap so that the UI matches the look of the Salesforce1 app.

With your first AngularJS and Bootstrap enabled Visualforce page now working you are ready to build modern web apps on Salesforce!  Let us know how it goes.
