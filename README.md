# .NET CLI Cheatsheet

This intended to be a quick reference to what I consider to be the most useful `dotnet` commands.

## `dotnet new`

Creates a new project, configuration file, or solution based on the specified template.

Project creation example: 
```ps1
dotnet new webapi -n "MyWebApi"
```

Solution creation example:
```ps1
dotnet new sln -n "MySolution"
```

Configuration file creation example:
```ps1
dotnet new editorconfig
```

## `dotnet build`

Builds a project and all of its dependencies into a set of binaries. The binaries include the project's code in Intermediate Language files with a .dll extension.

## `dotnet publish`

Compiles the application, reads through its dependencies specified in the project file, and publishes the resulting set of files to a directory.

Framework-dependent cross-platform binary example:
```ps1
dotnet publish
```

Framework-dependent executable example:

```ps1
dotnet publish -r linux-x64 --self-contained false
```

Self-contained executable example:
```ps1
dotnet publish -r win-x64 --self-contained true
```

## `dotnet run`

 Runs source code without any explicit compile or launch commands.

 ## `dotnet test`

 .NET test driver used to execute unit tests.

 ## `dotnet clean`

 Cleans the output of the previous build of a project.

## `dotnet sln list`

Lists the projects in a .NET solution file.

## `dotnet sln add`

Adds one or more projects to the solution file.

Example: 

```ps1
dotnet sln "MySolution.sln" add .\MyWebApi\MyWebApi.csproj .\MyClassLib\MyClassLib.csproj
```

## `dotnet sln remove`

Removes a project or multiple projects from the solution file.

Example:
```ps1
dotnet sln "MySolution.sln" remove .\MyWebApi\MyWebApi.csproj .\MyClassLib\MyClassLib.csproj
```

## `dotnet add package`

Adds a package reference to a project file.

Example: 

```ps1
dotnet add .\MyWebApi\MyWebApi.csproj package Microsoft.EntityFrameworkCore
```

## `dotnet add reference`

Adds project to project reference.

Example: 

```ps1
dotnet add .\MyWebApi\MyWebApi.csproj reference .\MyClassLib\MyClassLib.csproj
```

## `dotnet remove package`

Removes package reference from a project file.

Example:

```ps1
dotnet remove .\MyWebApi\MyWebApi.csproj package Microsoft.EntityFrameworkCore 
```

## `dotnet remove reference`

Removes project to project reference.

Example:
```ps1
dotnet remove .\MyWebApi\MyWebApi.csproj reference .\MyClassLib\MyClassLib.csproj
```

## `dotnet list reference`

Lists project to project references.

Example:
```ps1
dotnet list .\MyWebApi\MyWebApi.csproj reference
```

___

Every definition and example is based on the [Microsoft Documentation]("https://docs.microsoft.com/en-us/dotnet/core/tools/").



