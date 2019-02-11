# OffensiveCSharp
This is a collection of C# tooling I've created for use on operations. All code is designed to be compatible with .NET 3.5 unless otherwise noted. Open each project's .SLN in Visual Studio and compile as "Release".

**AbandonedCOMKeys** - Enumerates abandoned COM keys (specifically `InprocServer32`). Useful for persistence as you can, in some cases, write to the missing location and call with `rundll32.exe -sta {CLSID}`. Technique referenced in [this post](https://bohops.com/2018/06/28/abusing-com-registry-structure-clsid-localserver32-inprocserver32/) by @bohops  
**CredPhisher** - Prompts the current user for their credentials using the `CredUIPromptForWindowsCredentials` WinAPI function. Supports an argument to provide the message text that will be shown to the user.  
**ImplantSSP** - Installs a user-supplied Security Support Provider (SSP) DLL on the system, which will be loaded by LSA on system start. You can also preload this in the assembly as a base64-encoded blob. Based on [Install-SSP](https://powersploit.readthedocs.io/en/latest/Persistence/Install-SSP/) by @mattifestation.  
**GPSCoordinates (.NET 4.0+)** - Tracks the system's GPS coordinates (accurate within 1km currectly) if Location Services are enabled. Works on Windows 10 currently, but hoping to cover all versions 7+.  
**SessionSearcher (.NET 4.0+)** - Searches all connected drives for PuTTY private keys and RDP connection files and parses them for relevant details. Based on [SessionGopher](https://github.com/Arvanaghi/SessionGopher) by @arvanaghi.  
