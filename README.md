ReSharperExtensions
===================
This solution contains Live Templates and macros for [JetBrains ReSharper](http://www.jetbrains.com/resharper/). You can check out an example template for MSTest in the ReSharper settings for this solution. The tm template allows you to write test method names as sentences with spaces, and the macro will replace the spaces with underscores as you type. It also allows you to select an MSTest category and assigns the current user as the owner of the test in a format compatible with TFS.

See [http://www.joaroyen.com/2010/08/resharpers-live-templates-can-do.html](http://www.joaroyen.com/2010/08/resharpers-live-templates-can-do.html) for more information.

Installation instructions
-------------------------

Alternative 1 is recommended if you want to tinker with and debug the macros yourself, while alternative 2 is easier if you just want to use the macros in your own templates.

### Alternative 1: Build from sources and install Debug build ###

* Download and install [ReSharper SDK](http://www.jetbrains.com/resharper/download/index.html)
* Open Visual Studio 2012 and build the solution in Debug configuration
* Close all instances of Visual Studio
* Run "Deploy.bat" from an elevated command prompt to copy dll and pdb to the ReSharper 7.0 plugins folder

### Alternative 2: From precompiled package with Release build ###

* Download the latest package from the download section on [GitHub](https://github.com/joaroyen/ReSharperExtensions/downloads).
* Unzip the package to an empty directory.
* Copy JoarOyen.ReSharperPlugIn.dll to the ReSharper 7.0 plugins folder. This will typically be something like "C:\Program Files (x86)\JetBrains\ReSharper\v7.0\Bin\Plugins\JoarOyen\".
* Open the "ReSharperExtensions.sln.DotSettings" file using "ReSharper -> Manage Options..." to inspect the example template

Comments
--------

* Master is updated to support ReSharper 7, and requires .NET 4.0 or newer. The macros can therefore only be used in VS2010 and VS2012.
* Macros that works with previous versions of ReSharper and Visual Studio are available in separate branches for each version of ReSharper.
* The code in this version is built with the ReSharper SDK, and the namespace for the macros has been changed to reflect the new name of the assembly.
* The test project is using NUnit from ReSharper SDK, but uses NuGet for NSubstitute (this dependency should be downloaded automatically).
* The Deploy.bat file must be run with administrative privileges if UAC is enabled
