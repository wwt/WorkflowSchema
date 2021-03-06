# Contributing to WorkflowSchema
Thank you for your interest in WorkflowSchema!

[![Issues](https://img.shields.io/github/issues/wwt/WorkflowSchema?color=bright-green)](https://github.com/wwt/WorkflowSchema/issues)
[![Pull Requests](https://img.shields.io/github/issues-pr/wwt/WorkflowSchema?color=bright-green)](https://github.com/wwt/WorkflowSchema/pulls)

## Updating the schema
If your contribution meets any of the below guidelines it's required that you add the appropriate label on the pull request.

#### Important note
Updating the version of the schema requires that all the libraries using the schema are updated to reflect the new version.
This includes [SwiftCurrent](https://github.com/wwt/SwiftCurrent).

### When to version
Using these labels will run a GitHub action that updates the version accordingly.
- **NO LABEL**: When there are just metadata changes that would not affect any parser in any library
- **NO LABEL**: When examples are updated
- **NO LABEL**: When descriptions are revamped
---
- **PATCH REQUIRED**: When any field that is parsed changed
- **PATCH REQUIRED**: When new fields are added
- **PATCH REQUIRED**: When the validation requirements for a field change (minLength > 0, etc...)
---
- **MINOR REQUIRED**: When a field name is changed
- **MINOR REQUIRED**: When a field type is changed
- **MINOR REQUIRED**: When a field is made parsable both as a string and as an object
---
- **MAJOR REQUIRED**: When we change a fundamental behavior (flowPersistence)
- **MAJOR REQUIRED**: When sequence is no longer what we use to describe workflows

### Minor label
- break to the existing api. `ex. changing the way that FlowRepresentableName works`

### Major label
- fundamental shift in design. `ex. [sequence] goes away and we decide on a new way to describe workflows`

## Submitting issues
### Filing bugs
If you found a bug in WorkflowSchema, thank you!  Please go to [issues](https://github.com/wwt/WorkflowSchema/issues/new/choose) and use the `Bug report` template to file it.  We'll reach out to you as soon as we can.  Some things the template will ask for are:
- Steps to reproduce
- Context around your environment
- Optional screenshots and debugging logs

### Feature requests
If you have an idea or change you would like to request, please go to [issues](https://github.com/wwt/WorkflowSchema/issues/new/choose) and use the `Feature request` template to make your request.  We'll reach out to you as soon as we can to discuss.  The more "why" you put into your request, the better we will be able to help build a solution that meets our styling and achieves your goals.

## Pull Requests
PRs have a checklist that walks you through the things that you should do for any PR. This document provides greater detail and context around what some of those checklist items mean. Please take the time to read through this document and our styleguide before contributing so that we can keep WorkflowSchema clean, and maintainable. By the time you submit code we want to be focused on the logic, not the formatting, or patterns.

> The WorkflowSchema team finds value in structuring our commit messages in a consistent way. We would love it if you would do the same:
>
> ```[branch-name] - description```

## Sign the CLA

Before you can contribute to WorkflowSchema, you will need to sign the [Contributor License Agreement](https://cla-assistant.io/wwt/WorkflowSchema).

## Code of Conduct

Please make sure to read and observe the [Code of Conduct](CODE_OF_CONDUCT.md).

## Style guide
We use [EditorConfig](https://editorconfig.org) for this repo. Your editor should support this out of the box, but if not there is likely a plugin you can use.
