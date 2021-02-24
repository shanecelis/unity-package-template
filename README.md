# Unity Package Template

This is a Unity Package Template made according to Unity's [layout convention](https://docs.unity3d.com/Manual/cus-layout.html). It works as a dotnet template.

## Installation

Install the template.

    $ git clone https://github.com/shanecelis/unity-package-template
    $ dotnet new --install unity-package-template
    
## Usage

Create a directory. Choose the name carefully; its name is your package's name.

    $ mkdir MyPackage
    $ cd MyPackage
    $ dotnet new unitypackage --company "My Company"
    
This creates the following files:

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

See Unity's documentation for ways that you can [share your package](https://docs.unity3d.com/Manual/cus-share.html).

## Technical Notes

### GUIDs

New GUIDs are generated on each invocation. However, if you're adding a new file to the template, remember to add its GUID to the `.template.config/template.json` file. If you're adding a lot of files, use the `.template.config/collect-guids` bash script to help.

## Acknowledgements

Thank you to Adam Graham of Zigurous for creating [unity-package-template](https://github.com/zigurous/unity-package-template), of which this is a fork.
