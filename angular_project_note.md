```text
1 ng build --configuration production
2 web.config file create
```
```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <system.webServer>

    <!-- Rewrite all non-file requests to index.html (for Angular routing) -->
    <rewrite>
      <rules>
        <rule name="Angular Routes" stopProcessing="true">
          <match url=".*" />
          <conditions logicalGrouping="MatchAll">
            <add input="{REQUEST_FILENAME}" matchType="IsFile" negate="true" />
            <add input="{REQUEST_FILENAME}" matchType="IsDirectory" negate="true" />
          </conditions>
          <action type="Rewrite" url="/index.html" />
        </rule>
      </rules>
    </rewrite>

    <!-- Static content MIME types -->
    <staticContent>
      <!-- .json is already defined in IIS, so we skip it -->
      <mimeMap fileExtension=".webmanifest" mimeType="application/manifest+json" />
    </staticContent>

  </system.webServer>
</configuration>

```

```text
3 iis server new server create 

```
