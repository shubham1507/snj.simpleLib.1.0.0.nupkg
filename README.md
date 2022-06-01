snj@snj-ThinkPad-T440p:~/SimpleLib$ nuget pack Package.nuspec
Attempting to build package from 'Package.nuspec'.
Successfully created package '/home/snj/SimpleLib/snj.simpleLib.1.0.0.nupkg'.

WARNING: 3 issue(s) found with package 'snj.simpleLib'.

Issue: Remove sample nuspec values.
Description: The value "Tag1 Tag2" for Tags is a sample value and should be removed.
Solution: Replace with an appropriate value or remove and it and rebuild your package.

Issue: Remove sample nuspec values.
Description: The value "Summary of changes made in this release of the package." for ReleaseNotes is a sample value and should be removed.
Solution: Replace with an appropriate value or remove and it and rebuild your package.

Issue: Remove sample nuspec values.
Description: The value "Package description" for Description is a sample value and should be removed.
Solution: Replace with an appropriate value or remove and it and rebuild your package.
snj@snj-ThinkPad-T440p:~/SimpleLib$  nuget setApiKey oy2d3pkmf3rpysf6d7yq4yisqxn2vogedcusahy76eqgcq
The API Key 'oy2d3pkmf3rpysf6d7yq4yisqxn2vogedcusahy76eqgcq' was saved for the NuGet gallery (https://www.nuget.org) and the symbol server (http://nuget.gw.symbolsource.org/Public/NuGet).





snj@snj-ThinkPad-T440p:~/SimpleLib$ dotnet nuget push snj.simpleLib.1.0.0.nupkg --api-key oy2d3pkmf3rpysf6d7yq4yisqxn2vogedcusahy76eqgcq --source https://api.nuget.org/v3/index.json
Command 'dotnet' not found, but can be installed with:
sudo snap install dotnet-sdk
snj@snj-ThinkPad-T440p:~/SimpleLib$ sudo snap install dotnet-sdk
[sudo] password for snj: 
error: This revision of snap "dotnet-sdk" was published using classic
       confinement and thus may perform arbitrary system changes outside of the
       security sandbox that snaps are usually confined to, which may put your
       system at risk.

       If you understand and want to proceed repeat the command including
       --classic.
snj@snj-ThinkPad-T440p:~/SimpleLib$ sudo snap install dotnet-sdk --classic
dotnet-sdk 6.0.300 from Microsoft .NET Core (dotnetcore*) installed
snj@snj-ThinkPad-T440p:~/SimpleLib$ dotnet nuget push snj.simpleLib.1.0.0.nupkg --api-key oy2d3pkmf3rpysf6d7yq4yisqxn2vogedcusahy76eqgcq --source https://api.nuget.org/v3/index.json

Welcome to .NET 6.0!
---------------------
SDK Version: 6.0.300

Telemetry
---------
The .NET tools collect usage data in order to help us improve your experience. It is collected by Microsoft and shared with the community. You can opt-out of telemetry by setting the DOTNET_CLI_TELEMETRY_OPTOUT environment variable to '1' or 'true' using your favorite shell.

Read more about .NET CLI Tools telemetry: https://aka.ms/dotnet-cli-telemetry

----------------
Installed an ASP.NET Core HTTPS development certificate.
To trust the certificate run 'dotnet dev-certs https --trust' (Windows and macOS only).
Learn about HTTPS: https://aka.ms/dotnet-https
----------------
Write your first app: https://aka.ms/dotnet-hello-world
Find out what's new: https://aka.ms/dotnet-whats-new
Explore documentation: https://aka.ms/dotnet-docs
Report issues and find source on GitHub: https://github.com/dotnet/core
Use 'dotnet --help' to see available commands or visit: https://aka.ms/dotnet-cli
--------------------------------------------------------------------------------------
Segmentation fault (core dumped)
snj@snj-ThinkPad-T440p:~/SimpleLib$ Pushing snj.simpleLib.1.0.0.nupkg to 'https://www.nuget.org/api/v2/package'...
  PUT https://www.nuget.org/api/v2/package/
warn : All published packages should have license information specified. Learn more: https://aka.ms/nuget/authoring-best-practices#licensing.
  Created https://www.nuget.org/api/v2/package/ 1661ms
Your package was pushed.


https://medium.com/@pampas93/create-upload-install-a-nuget-package-using-nuget-cli-d7719a103a03