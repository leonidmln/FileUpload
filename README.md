# Uploading large files in ASP.NET Core
This project demonstrate how to upload large files in ASP.NET Core 2.0 and display progress bar.
No 3rd party scripts or libraries
If you use IIS or IIS Express not Kestrel, then you should to change config file
<requestLimits maxAllowedContentLength="50000000" />
