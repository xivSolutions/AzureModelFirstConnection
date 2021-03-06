Connection String Template 
-------------------------------------
for Windows Azure/EF Model-First Database
-----------------------------------------------------------

Sometimes we need to develop using Entity Framework in a Model First or Database-First context. If we deploy a website using EF Model First to Windows Azure Websites, the connection string and configuration can be finicky, and it can be difficult to tell what we are doing wrong. 

The connection string pattern below can be used directly in the Azure Website Connection String Configuration settings, after replacing the `<angle bracketed>` items with your own values (replace the angle brackets too - they are not part of the connection string). 

Name the connection string in the configuration panel to match the Model-First Connection string in your Web Application. 
<dl>
  <dt>The Azure Connection String for Model-First Connection:</dt>
</dl>

```
    metadata=res://*/Models.<EFModel>.csdl|res://*/Models.<EFModel>.ssdl|res://*/Models.<EFModel>.msl;provider=System.Data.SqlClient;provider connection string="data source=tcp:<AzureServer>.database.windows.net;initial catalog=<AzureDatabaseName>;Persist Security Info=True;User ID=<UserLogIn>@<AzureServer>;Password=<UserPassword>"
```

For more information, see the related post:

[ASP.NET MVC–Azure Websites and EF Model First Connection Strings when Deploying from Github](http://typecastexception.com/post/2013/10/20/ASPNET-MVC%E2%80%93Azure-Websites-Azure-SQL-Database-and-EF-Model-FirstDatabase-First-Connection-Strings-when-Deploying-from-Github.aspx)


