if you use everything should be ok,
but if you use IIS or IIS Express
you should to change web.config, owerthise you will see error 

HTTP 404.13 - Not Found
The request filtering module is configured to deny a request that exceeds the request content length.

IIS - change web.config
<system.webServer>
  <security>
    <requestFiltering>
      <!-- This will handle requests up to 50MB -->
      <requestLimits maxAllowedContentLength="52428800" />
    </requestFiltering>
  </security>
</system.webServer>

IIS Express - you should change applicationhost.config
how to find applicationhost.config if you use IIS Express
https://stackoverflow.com/questions/12946476/where-is-the-iis-express-configuration-metabase-file-found