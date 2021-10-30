# Swagger API:

- https://habr.com/ru/company/microsoft/blog/325872/
- https://blog.georgekosmidis.net/2020/07/11/swagger-in-asp-net-core-tips-and-tricks/

```
<PropertyGroup>
  <GenerateDocumentationFile>true</GenerateDocumentationFile>
</PropertyGroup>
```

```
services.AddSwaggerGen(x =>
{
    var xmlFile = $"{Assembly.GetExecutingAssembly().GetName().Name}.xml";
    var xmlPath = Path.Combine(AppContext.BaseDirectory, xmlFile);
    c.IncludeXmlComments(xmlPath);
});
```
