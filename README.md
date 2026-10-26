# Workbench Assistant: releases

This repository holds only built update packages and update manifests for the Workbench Assistant add-in for Autodesk Revit. There is no source code here.

- `manifest-<year>.json` (one per Revit year, 2023 to 2027) lists the packages and data updates for that year. The add-in's loader reads it from
  `https://raw.githubusercontent.com/Jackieson888/workbench-assistant-releases/main/manifest-<year>.json`.
- Each package is a zip attached to a GitHub Release (`vX.Y.Z`). The manifest gives its download URL and SHA-256 hash; the loader rejects any download whose hash doesn't match.

Packages are published with `installer/publish-release.ps1` (code) and `installer/publish-data.ps1` (data only) in the source repository. Don't edit the manifests by hand unless you're removing a bad version.

Copyright (c) 2026 Jackson Schacher. All rights reserved. Being able to download a package here doesn't grant a license to use it.
