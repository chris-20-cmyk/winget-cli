## Bug Fixes

### Correlate an installed package when one catalog package publishes its version

`winget list` and `winget upgrade` can match an installed package when several catalog packages share a strong identifier, such as a product code, and the installed version is published by only one of them. A non-empty installed channel must match that version. If the version is published by more than one package, or by none, the installed entry stays uncorrelated. An explicit package id still selects the requested package. A package id already recorded in the local tracking catalog is not replaced by the version comparison. Manifest upgrade denial and an existing explicit-upgrade pin are unchanged.

