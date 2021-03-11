# Puppeteer Fork 

The present repository contains information and a partial restoration of `new-docs/` aimed to help the development of [**#6118**](https://github.com/puppeteer/puppeteer/issues/6118).

My personal fork of Puppeteer can be found [**here.**](https://github.com/lumbridge01/puppeteer)

## ℹ️ Information

A partially restored version of `new-docs/` has been included, containing the first 50 files from [**new-docs@e655bb6ca2@puppeteer/puppeteer**](https://github.com/puppeteer/puppeteer/tree/e655bb6ca22e559ae95f3342a5ad5e954ce4649f), which is the last commit before they where removed from the repository to be generated via CI. 

> chore: gitignore new-docs (#6511) - They are generating a lot of noise in PRs. This commit removes them from git, but updates CI to generate them - to ensure there are no errors when generating the new documentation. [**637a1f7409@puppeteer/puppeteer**](https://github.com/puppeteer/puppeteer/commit/637a1f740902aaa375713e5e29417e453e3f9b80)

To obtain the current docs, the Actions Workflow runs:

```
npm run generate-docs
```

## 🚨 Important

Note that some `docs(*)` commits were introduced in the span of Oct 14, 2020 to this day, so some files in `new-docs/` most likely are not exactly the same as the ones that are to be generated with the updated `api.md` file. The files are included with the sole purpose of understanding the previous documentation structure, and are only partially restored as the total ammount is over 4000 files.

Finally, don't forget to follow [CONTRIBUTING.MD](https://github.com/puppeteer/puppeteer/blob/main/CONTRIBUTING.md) and run the doc linter.

```
Writing Documentation

All public API should have a descriptive entry in docs/api.md. 
There's a documentation linter which makes sure documentation is aligned with the codebase.

To run the documentation linter, use:

npm run doc
```

## 📋 Issues

One of the active tasks is to _Fix any API Extractor warnings_, to achieve this I have structured them in the following todo list, taking the output from the last Actions Workflow on main.

```
Using configuration from ./api-extractor.json
Analysis will use the bundled TypeScript version 4.1.5
*** The target project appears to use TypeScript 4.2.3 which is newer than the bundled compiler engine; 
consider upgrading API Extractor.
Writing: /home/runner/work/puppeteer/puppeteer/temp/puppeteer.api.json
Writing package typings: /home/runner/work/puppeteer/puppeteer/lib/types.d.ts
```

* [ ] Warning: node_modules/devtools-protocol/types/protocol-mapping.d.ts:443:86 - (tsdoc-code-span-missing-delimiter) The code span is missing its closing backtick
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:4117:73 - (tsdoc-undefined-tag) The TSDoc tag "@media" is not defined in this configuration
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:4118:32 - (tsdoc-undefined-tag) The TSDoc tag "@import" is not defined in this configuration
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:4128:37 - (tsdoc-at-sign-in-word) The "@" character looks like part of a TSDoc tag; use a backslash to escape it
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:4128:47 - (tsdoc-characters-after-block-tag) The token "@import" looks like a TSDoc tag but contains an invalid character ")"; if it is not a tag, use a backslash to escape the "@"
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:7926:53 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:7926:68 - (tsdoc-malformed-html-name) Invalid HTML element: An HTML name must be an ASCII letter followed by zero or more letters, digits, or hyphens
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9188:68 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9188:53 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9294:68 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9294:53 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9367:32 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9367:53 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9873:68 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:9873:53 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11026:99 - (tsdoc-code-span-missing-delimiter) The code span is missing its closing backtick
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11027:24 - (tsdoc-code-span-missing-delimiter) The code span is missing its closing backtick
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11229:63 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11230:63 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11594:97 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:11594:50 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:12564:86 - (tsdoc-code-span-missing-delimiter) The code span is missing its closing backtick
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:14142:32 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:14142:53 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: node_modules/devtools-protocol/types/protocol.d.ts:14258:68 - (tsdoc-unnecessary-backslash) A backslash can only be used to escape a punctuation character
* [ ] Warning: src/common/Browser.ts:183:3 - (ae-forgotten-export) The symbol "BrowserCloseCallback" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Browser.ts:554:1 - (ae-missing-release-tag) "BrowserContextEmittedEvents" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Browser.ts:608:1 - (ae-missing-release-tag) "BrowserContext" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Connection.ts:47:3 - (ae-forgotten-export) The symbol "ConnectionTransport" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Connection.ts:53:3 - (ae-forgotten-export) The symbol "ConnectionCallback" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Connection.ts:70:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Connection.ts:70:13 - (tsdoc-param-tag-with-invalid-type) The @param block should not include a JSDoc-style '{type}'
* [ ] Warning: src/common/Connection.ts:71:27 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: src/common/Connection.ts:71:15 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: src/common/Connection.ts:170:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Connection.ts:170:13 - (tsdoc-param-tag-with-invalid-type) The @param block should not include a JSDoc-style '{type}'
* [ ] Warning: src/common/Connection.ts:171:36 - (tsdoc-escape-greater-than) The ">" character should be escaped using a backslash to avoid confusion with an HTML tag
* [ ] Warning: src/common/Connection.ts:171:37 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: src/common/Connection.ts:171:24 - (tsdoc-malformed-html-name) Invalid HTML element: Expecting an HTML name
* [ ] Warning: src/common/Connection.ts:171:15 - (tsdoc-malformed-inline-tag) Expecting a TSDoc tag starting with "{@"
* [ ] Warning: src/common/Connection.ts:245:3 - (ae-forgotten-export) The symbol "ProtocolMapping" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Connection.ts:277:3 - (ae-forgotten-export) The symbol "CDPSessionOnMessageObject" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/ConsoleMessage.ts:42:1 - (ae-missing-release-tag) "ConsoleMessageType" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Coverage.ts:109:3 - (ae-forgotten-export) The symbol "JSCoverage" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Coverage.ts:113:3 - (ae-forgotten-export) The symbol "CSSCoverage" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/DeviceDescriptors.ts:1034:1 - (ae-missing-release-tag) "DevicesMap" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/DeviceDescriptors.ts:1035:3 - (ae-forgotten-export) The symbol "Device" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/DeviceDescriptors.ts:1038:7 - (ae-missing-release-tag) "devicesMap" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Dialog.ts:42:1 - (ae-missing-release-tag) "Dialog" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Errors.ts:37:1 - (ae-forgotten-export) The symbol "CustomError" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Errors.ts:37:1 - (ae-missing-release-tag) "PuppeteerErrors" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Errors.ts:39:14 - (ae-missing-release-tag) "puppeteerErrors" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/EvalTypes.ts:24:1 - (ae-missing-release-tag) "UnwrapPromiseLike" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/EventEmitter.ts:11:3 - (ae-forgotten-export) The symbol "EventType" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/EventEmitter.ts:11:3 - (ae-forgotten-export) The symbol "Handler" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/EventEmitter.ts:38:1 - (ae-incompatible-release-tags) The symbol "EventEmitter" is marked as @public, but its signature references "CommonEventEmitter" which is marked as @internal
* [ ] Warning: src/common/ExecutionContext.ts:26:14 - (ae-missing-release-tag) "EVALUATION_SCRIPT_URL" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/ExecutionContext.ts:36:7 - (tsdoc-reference-missing-dot) Expecting a period before the next component of a declaration reference
* [ ] Warning: src/common/ExecutionContext.ts:129:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/ExecutionContext.ts:130:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/ExecutionContext.ts:181:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/ExecutionContext.ts:182:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/ExecutionContext.ts:347:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/FileChooser.ts:38:1 - (ae-missing-release-tag) "FileChooser" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/JSHandle.ts:36:1 - (ae-missing-release-tag) "BoxModel" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/LifecycleWatcher.ts:30:1 - (ae-missing-release-tag) "PuppeteerLifeCycleEvent" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/LifecycleWatcher.ts:55:3 - (ae-forgotten-export) The symbol "ProtocolLifeCycleEvent" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/LifecycleWatcher.ts:60:3 - (ae-forgotten-export) The symbol "PuppeteerEventListener" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/NetworkManager.ts:45:1 - (ae-missing-release-tag) "InternalNetworkConditions" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/Page.ts:286:34 - (tsdoc-characters-after-inline-tag) The character "." cannot appear after the TSDoc tag name; expecting a space
* [ ] Warning: src/common/Page.ts:286:63 - (tsdoc-escape-right-brace) The "}" character should be escaped using a backslash to avoid confusion with a TSDoc inline tag
* [ ] Warning: src/common/Page.ts:983:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Page.ts:986:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Page.ts:989:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Page.ts:1416:9 - (ae-forgotten-export) The symbol "MediaFeature" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/Page.ts:1464:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Page.ts:1465:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Page.ts:1466:6 - (tsdoc-param-tag-missing-hyphen) The @param block should be followed by a parameter name and then a hyphen
* [ ] Warning: src/common/Puppeteer.ts:42:1 - (ae-missing-release-tag) "ConnectOptions" is exported by the package, but it is missing a release tag (@alpha, @beta, @public, or @internal)
* [ ] Warning: src/common/WebWorker.ts:72:3 - (ae-forgotten-export) The symbol "ConsoleAPICalledCallback" needs to be exported by the entry point api-docs-entry.d.ts
* [ ] Warning: src/common/WebWorker.ts:72:3 - (ae-forgotten-export) The symbol "ExceptionThrownCallback" needs to be exported by the entry point api-docs-entry.d.ts

The complete output can be found [here](https://github.com/puppeteer/puppeteer/runs/2064368112).
