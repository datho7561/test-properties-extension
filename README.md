# test-properties-extension

This is a vscode extension for testing purposes.

Ignore validation of `helidon.*` properties in `microprofile-config.properties` through jdt.ls extension.

## Repo Layout

| Folder | Contains |
|-|-|
| `/` | vscode extension
| `/server ` | jdt.ls extension

## Developing and Using

 * **REQS**: need java11 with JAVA_HOME set, and maven on path
 * Compile the jdt.ls extension through npm script (unix only sorry):
    * `npm run buildServer`
 * Compile the jdt.ls extension manually:
    * Run `mvn verify` in `server` directory
    * Copy `removevalidation.core/target/removevalidation.core-1.0.0.jar` to `bundledServer/removevalidation.core.jar`
 * Make a vsix: `vsce package`