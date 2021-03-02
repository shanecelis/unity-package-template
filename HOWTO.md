# HOWTO

Remind myself how to do the maintenance of this package.

## How to package nupkg?

   $ nupkg pack .nuspec

## How to inspect package?

   $ unzip -l SeawispHunter.Unity3D.Package.Template.0.1.1.nupkg

## How to upload package?

   $ dotnet nuget push SeawispHunter.Unity3D.Package.Template.0.1.1.nupkg --source https://api.nuget.org/v3/index.jso

## How to generate the file tree?

   $ tree -I '*.meta' | pbcopy
