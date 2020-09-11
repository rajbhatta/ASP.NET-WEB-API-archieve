## How connection String is managed in .NET ##
```java
<connectionStrings>  
   <add name="mytest" connectionString="Data Source=.\SQLEXPRESS;Initial Catalog=mytest;Integrated Security=True;" providerName="System.Data.SqlClient" />  
   <add name="Northwind" connectionString="Data Source=.\SQLEXPRESS;Initial Catalog=Northwind;Integrated Security=True;" providerName="System.Data.SqlClient" />  
   <add name="Northwind" connectionString="Data Source=.\SQLEXPRESS;Initial Catalog=databasename;uid=sa;pwd=sa;" providerName="System.Data.SqlClient" />  
</connectionStrings>  
```

```c#
1. <add name="mytest" connectionString="Data Source=.\SQLEXPRESS;Initial Catalog=mytest;Integrated Security=True;" providerName="System.Data.SqlClient" />  
Data Source= Data source is the name of the MS SQL server instance you are connecting to
Initial Catalog=Database name
```

## How to see all possible connection string in ASP.NET WEB API ##
```java
- View -> Server Explorer.
- Expand Data Connections.
```
## How to create new connection in ASP.NET WEB API

### References ###
https://www.c-sharpcorner.com/UploadFile/7d3362/various-ways-to-specify-connection-string-in-Asp-Net-web-app/
