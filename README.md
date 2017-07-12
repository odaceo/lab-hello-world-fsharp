# Lab :: Hello World :: F# Application on Linux

[![License](https://img.shields.io/github/license/odaceo/lab-hello-world-fsharp.svg)](LICENSE)
[![Build Status](https://travis-ci.org/odaceo/lab-hello-world-fsharp.svg)](https://travis-ci.org/odaceo/lab-hello-world-fsharp)

## Description

A simple F# application on Linux.

## Prerequisites

[Vagrant](https://www.vagrantup.com/downloads.html) must be installed on your 
computer to mount the workbench for this project.

Open a Terminal and run the following commands:

```shell
vagrant up
vagrant ssh
cd /vagrant
```

## Restoring dependencies

The restore command download dependencies specified in the .NET project.

``` shell
dotnet restore
```

## Compiling the application

The publish command produces binary files you can run without intalled .NET Core runtime.
Use the following command for the current operating system and architecture:

``` shell
dotnet publish -c release
```

## Running the application

To launch the application use the following command:

``` shell
./bin/release/netcoreapp1.1/ubuntu.16.04-x64/publish/hello Odaceo
```

## What we learned

### Creating a Console application

Use the following command to create a simple Hello World application:

``` shell
dotnet new console --language F#
```

### Compiling the application for another operating system

Reference the macOS Sierra runtime in the `hello.csproj` file:

``` xml
    <RuntimeIdentifiers>ubuntu.16.04-x64;osx.10.12-x64</RuntimeIdentifiers>
```

And then use the following command for building macOS Sierra binaries:

``` shell
dotnet publish -c release -r osx.10.12-x64
```

See [the Self-contained deployments documentation](https://docs.microsoft.com/en-us/dotnet/articles/core/deploying/index#self-contained-deployments-scd) for more details.

## Reporting Issues

Issues can be reported at [https://github.com/odaceo/lab-hello-world-fsharp/issues](https://github.com/odaceo/lab-hello-world-fsharp/issues)

## Source code

The source code is available at [https://github.com/odaceo/lab-hello-world-fsharp](https://github.com/odaceo/lab-hello-world-fsharp)

## License

All the source code is distributed under [ASL 2.0](LICENSE).

## Copyright

© 2017 [Odaceo](http://odaceo.ch). All rights reserved.
