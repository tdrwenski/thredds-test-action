# THREDDS Test action

This action is used to run the tests of the various THREDDS projects in an environment that matches our Jenkins server instance.
More information on that environment can be found at <https://github.com/Unidata/thredds-test-environment>.

## Inputs

### java-vendor

* **Required**: Vendor of java to use when running the tests (temurin or zulu)

### java-version

* **Required**: Version of java to use when running the tests (8, 11, or 14)

### build-tool

* **Required**: Name of build tool used to run the tests (gradlew or mvn)

### test-command

* **Required**: Command used in conjunction with the build tool to run the tests.

## Example usage

~~~yml
uses: Unidata/thredds-test-action@v1
with:
  java-vendor: 'temurin'
  java-version: '11'
  build-tool: 'gradlew'
  test-command: 'clean testAll'
~~~
