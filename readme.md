ErrorHandlerMvc
===
by [Daniel Calkins](http://dcalkins.com) - [Contact Email](mailto:dan@dcalkins.com)


[![dcalkins MyGet Build Status](https://www.myget.org/BuildSource/Badge/dcalkins?identifier=017b9443-736d-4f29-b98c-27d23b05df60)](https://www.myget.org/)

Provides a user-friendly error page whenever a controller, action or route is not found or encounters an error in your ASP.NET MVC3/MVC4/MVC5 application.
A view called NotFound or Error is rendered instead of the default ASP.NET error page.

How to use
----------
All you need to do is add the nuget package to your project and you will be set. The reference is all that is needed to install ErrorHandlerMvc. ErrorHandlerMvc automatically installs itself during web application start-up. You can customize the NotFound and Error pages if you'd like.

Add via nuget using:
Install-Package ErrorHandlerMvc

[![Download on NuGet](https://raw.githubusercontent.com/ServiceStack/Assets/master/img/release-notes/install-ormlite.png)](https://www.nuget.org/packages/ErrorHandlerMvc/)

Details
-------
It handles all the different ways a 404 HttpException is usually thrown by ASP.NET MVC. This includes a missing controller, action and route. 
It will also handle any exceptions thrown from your code during actions to prevent the default ASP.NET error page. 

A catch-all route is added to the end of RouteTable.Routes.
The controller factory is wrapped to catch when controller is not found or encounters an error.
The action invoker of Controller is wrapped to catch when the action method is not found or encounters an error.
