# Unity Package Template

This is a Unity Package Template made according to Unity's [layout convention](https://docs.unity3d.com/Manual/cus-layout.html). It works as a dotnet template.

## Installation

Install the template from NuGet or from a cloned repository.

### Install from NuGet

Install the template from NuGet.

    $ dotnet new --install SeawispHunter.Unity3D.Package.Template

### Install from repository

Install the template from git repo.

    $ git clone https://github.com/shanecelis/unity-package-template
    $ dotnet new --install unity-package-template
    

## Usage

Create a directory. Choose the name carefully; its name is your package's name.

    $ mkdir MyPackage
    $ cd MyPackage
    $ dotnet new unitypackage --company "My Company"

This creates the following files (meta files excluded for clarity):


    MyPackage
    ├── CHANGELOG.md
    ├── Documentation~
    │   └── MyPackage.md
    ├── Editor
    │   ├── EditorExample.cs
    │   └── MyCompany.MyPackage.Editor.asmdef
    ├── LICENSE.md
    ├── README.md
    ├── Runtime
    │   ├── MyCompany.MyPackage.asmdef
    │   └── RuntimeExample.cs
    ├── Samples~
    │   ├── Sample 1
    │   │   └── Sample1.cs
    │   └── Sample 2
    │       └── pic.png
    ├── Tests
    │   ├── Editor
    │   │   ├── EditorExampleTest.cs
    │   │   └── MyCompany.MyPackage.Editor.Tests.asmdef
    │   └── Runtime
    │       ├── MyCompany.MyPackage.Tests.asmdef
    │       └── RuntimeExampleTest.cs
    └── package.json

The generated package name is "com.mycompany.mypackage" but edit that to your liking. Many values are only located within the `package.json` file, like the package description. It's expected that you will edit it after generation.

    $ $EDITOR package.json

## Using the Package

See Unity's documentation for ways that you can [share your package](https://docs.unity3d.com/Manual/cus-share.html) or the template's [README](_README.md).

## Technical Notes

### GUIDs

New GUIDs are generated on each invocation so there will be no meta file conflicts with separate packages. However, if you're adding a new file to this template, remember to add its GUID to the `.template.config/template.json` file. If you're adding a lot of files, use the `.template.config/collect-guids` bash script to help.

## Tips

The `Samples~` directory can be difficult to work when developing your package since Unity will not import it because it has the tilde suffix. One tip for Unix users is to make a symbolic link when you're developing your samples like this:

    $ ln -s Samples\~ Samples

You may want to add `Samples` and `Samples.meta` to your `.gitignore` file.

## Acknowledgements

Thank you to [Adam Graham](https://twitter.com/Zigurous) of [Zigurous](https://zigurous.com) for creating [unity-package-template](https://github.com/zigurous/unity-package-template), of which this is a fork.
