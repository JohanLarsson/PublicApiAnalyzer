# Public API Analyzer

[![NuGet](https://img.shields.io/nuget/v/DotNetAnalyzers.PublicApiAnalyzer.svg)](https://www.nuget.org/packages/DotNetAnalyzers.PublicApiAnalyzer) [![NuGet Beta](https://img.shields.io/nuget/vpre/DotNetAnalyzers.PublicApiAnalyzer.svg)](https://www.nuget.org/packages/DotNetAnalyzers.PublicApiAnalyzer)

[![Join the chat at https://gitter.im/DotNetAnalyzers/PublicApiAnalyzer](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/DotNetAnalyzers/PublicApiAnalyzer?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

[![Build status](https://ci.appveyor.com/api/projects/status/27963rsy48aseywm/branch/master?svg=true)](https://ci.appveyor.com/project/sharwell/publicapianalyzer/branch/master)

[![codecov.io](http://codecov.io/github/DotNetAnalyzers/PublicApiAnalyzer/coverage.svg?branch=master)](http://codecov.io/github/DotNetAnalyzers/PublicApiAnalyzer?branch=master)

The purpose of this analyzer is to write the public API to two text files, PublicAPI.Unshipped.txt and PublicAPI.Shipped.txt. Add the files to source control to keep track of how the API evolves.

## Using Public API Analyzer

The preferable way to use this package is to add the NuGet package [DotNetAnalyzers.PublicApiAnalyzer](http://www.nuget.org/packages/DotNetAnalyzers.PublicApiAnalyzer/)
to the project where you want to enforce rules.

The severity of individual rules may be configured using [rule set files](https://msdn.microsoft.com/en-us/library/dd264996.aspx)
in Visual Studio.

### In development

Use the code fix to update PublicAPI.Unshipped.txt.

### When releasing

1. Delete the contents of PublicAPI.Unshipped.txt and PublicAPI.Shipped.txt.
2. Use the code fix to write the publid API to PublicAPI.Unshipped.txt.
3. Cut the contents of PublicAPI.Unshipped.txt and paste it to PublicAPI.Shipped.txt.
The result should be empty PublicAPI.Unshipped.txt and complete PublicAPI.Unshipped.txt.

## Team Considerations

If you use older versions of Visual Studio in addition to Visual Studio 2015, you may still install these analyzers. They will be automatically disabled when you open the project back up in Visual Studio 2013 or earlier.

## Contributing

See [Contributing](CONTRIBUTING.md)
