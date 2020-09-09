## Getting started with ASP.NET ##

### 1. How to create a ASP.NET WEB API ###
<img src="Step1.png" />

### 2. How to select web API ###
<img src="Step2.png" />

### 3. Project Structure ###
This project is same as default MVC project with two specific files for Web API, WebApiConfig.cs in <b>App_Start </b> folder and ValuesController.cs in Controllers folder as shown below.

<img src="Step3.png"/>

### 4. What is inside WebApiConfig.cs and how it works? ###
```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Web.Http;

namespace WebApplication1
{
    public static class WebApiConfig
    {
        public static void Register(HttpConfiguration config)
        {
            // Web API configuration and services

            // Web API routes
            config.MapHttpAttributeRoutes();

            config.Routes.MapHttpRoute(
                name: "DefaultApi",
                routeTemplate: "api/{controller}/{id}",
                defaults: new { id = RouteParameter.Optional }
            );
        }
    }
}
```


### 5. How to write HTTP request such as GET, POST, PUT ? ###


### References ### 
https://www.tutorialsteacher.com/webapi/create-web-api-project
<br/>
https://www.youtube.com/watch?v=iaeHaydhatE
