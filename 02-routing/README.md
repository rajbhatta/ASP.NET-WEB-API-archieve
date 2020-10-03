## 1. How to work with routing in ASP.NET WEB API ##
### 1.1. User controller in ASP.NET ###
```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Net;
using System.Net.Http;
using System.Web.Http;

namespace MessgeWithSendGrid.Controllers
{
    public class UserController : ApiController
    {
        public String getUser()
        {
            return "TestUser";
        }
        
        public String getUserId(int id)
        {
            return "TestUser"+id;
        }

    }
}
```

### 1.2 How to access UserController ? ###
Access first method:
<br/>
http://localhost:50783/api/user


Access second method:
<br/>
http://localhost:50783/api/user/5

## 2. How to create HTTP verbs
```java
[HttpGet]
[HttpPut]
[HttpPost]
[HttpDelete]
[HttpHead]
[HttpOptions]
[HttpPatch]
```

### 2.1 How to implement [HttpGet] ###
```c#
using System;
using System.Collections.Generic;
using System.Linq;
using System.Net;
using System.Net.Http;
using System.Web.Http;

namespace MessgeWithSendGrid.Controllers
{
    public class UserController : ApiController
    {
        [HttpGet]
        public String testUser()
        {
            return "TestUser";
        }
        
         [HttpGet]
        public String deleteUser(int id)
        {
            return "TestUser"+id;
        }

    }
}
```

How to access it
<br/>
http://localhost:50783/api/user

How to access it
<br/>
http://localhost:50783/api/user/5

## 3. How to use HttpVerb with @Route (attribute routing) ##
### 3.1 What is attribute based routing in APS.NET ###

<b> Problems </b>

Unfortunately, convention-based routing makes it hard to support certain URI patterns that are common in RESTful APIs. For example, resources often contain child resources: Customers have orders, movies have actors, books have authors, and so forth. It's natural to create URIs that reflect these relations:

/customers/1/orders


<b> Solutions </b>

This type of URI is difficult to create using convention-based routing. Although it can be done, the results don't scale well if you have many controllers or resource types.

With attribute routing, it's trivial to define a route for this URI. You simply add an attribute to the controller action:

[Route("customers/{customerId}/orders")]
public IEnumerable<Order> GetOrdersByCustomer(int customerId) { ... }


