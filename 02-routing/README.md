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

    }
}
```

How to access it
<br/>
http://localhost:50783/api/user


