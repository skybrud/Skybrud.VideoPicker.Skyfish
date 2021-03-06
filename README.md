# Skybrud.VideoPicker.Skyfish

Skyfish add-on for our [Skybrud.VideoPicker](https://github.com/skybrud/Skybrud.VideoPicker) package for Umbraco 8.

## Installation

1. [**NuGet Package**][NuGetPackage]  
Install this NuGet package in your Visual Studio project. Makes updating easy.

1. [**ZIP file**][GitHubRelease]  
Grab a ZIP file of the latest release; unzip and move the contents to the root directory of your web application.

[NuGetPackage]: https://www.nuget.org/packages/Skybrud.VideoPicker.Skyfish/
[GitHubRelease]: https://github.com/skybrud/Skybrud.VideoPicker.Skyfish/releases/latest



## Configuration

Access to the Skyfish API requires a public key, secret key, username and a password. The Skyfish provider from this package can be configured as following:

```xml
<?xml version="1.0" encoding="utf-8" ?>
<settings>
	<providers>
		<skyfish>
			<credentials 
				id="00000000-0000-0000-0000-000000000000"
				name="My Skyfish credentials"
				apiKey="secret api key here"
				apiSecret="secret api secret here"
				username="your skyfish username"
				password="your skyfish password"/>
		</skyfish>
	</providers>
</settings>
```

With the current implementation, the provider will always use the first set of `<credentials>`, meaning multiple `<credentials>` elements are not directly supported.