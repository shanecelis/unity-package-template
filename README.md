# Unity Package Template

This is a Unity Package Template made according to Unity's [layout convention](https://docs.unity3d.com/Manual/cus-layout.html). It works with dotnet templates.

## Installation

    $ dotnet new --install unity-package-template
    
## Usage

    $ mkdir MyPackage
    $ cd MyPackage
    $ dotnet new unitypackage -c "My Company"
    
This template does not try to set every possible thing within the template. If it's only located within the `package.json` file---like the package description---then you're expected to edit it there.
    
    $ $EDITOR package.json
    
## Using the Package

The Unity Package Manager can load a package from a Git repository on a remote server.

To load a package from a Git URL:

1. Open the Package Manager window.
2. Click the add (`+`) button in the status bar.
3. Select **Add package from git URL** from the add menu.
4. Enter its Git URL in the text box and click `Add**.

## Technical Notes

### GUIDs

New GUIDs are generated on each invocation. However, if you're adding a new file to the template, remember to add its GUID to the `.template.config/template.json` file. If you're adding a lot of files, use the `.template.config/collect-guids` bash script to help.

## Acknowledgements

Thank you to Adam Graham of Zigurous for creating [unity-package-template](https://github.com/zigurous/unity-package-template), which this is a fork of.
