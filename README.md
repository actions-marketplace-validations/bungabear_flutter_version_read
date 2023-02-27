## Run
```
name: Test CI

on:
  push:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Get Flutter Version
      id: flutter_version
      uses: bungabear/flutter_version_read@main

    - name: Flutter App Version Number
      run: echo 'version_number:' ${{ steps.flutter_version.outputs.version_number }}
      
    - name: Flutter App Build Number
      run: echo 'build_number:' ${{ steps.flutter_version.outputs.build_number }}
      
    - name: Flutter App Version Number Major
      run: echo 'version_number_major:' ${{ steps.flutter_version.outputs.version_number_majojr }}
      
    - name: Flutter App Version Number Minor
      run: echo 'version_number:' ${{ steps.flutter_version.outputs.version_number_minor }}
      
    - name: Flutter App Version Number Patch
      run: echo 'version_number:' ${{ steps.flutter_version.outputs.version_number_patch }}

```


## How to build
```
npm install
npx webpack
```