# Welcome

This project provides a schema to validate your data driven workflows for [SwiftCurrent](https://github.com/wwt/SwiftCurrent). You can validate your json using a tool like [this online json schema validator](https://www.jsonschemavalidator.net).

## Examples

<details>
    <summary><b>The simplest implementation with a `FlowRepresentable` and its provided name.</b></summary>

```json
{
  "schemaVersion": "v0.0.1",
  "sequence": [
    {
      "flowRepresentableName": "FR1"
    }
  ]
}
```
</details>

<details>
    <summary><b>A more complex implementation that provides an optional `LaunchStyle` and `FlowPersistence`.</b></summary>

```json
{
  "schemaVersion": "v0.0.1",
  "sequence": [
    {
      "flowRepresentableName": "FR2",
      "launchStyle": "modal",
      "flowPersistence": "removedAfterProceeding"
    }
  ]
}
```
</details>

<details>
    <summary><b>An even more complex implementation that includes platform specifications.</b></summary>

```json
{
  "schemaVersion": "v0.0.1",
  "sequence": [
    {
      "flowRepresentableName": {
        "watchOS": "FR3",
        "macOS": "FR3",
        "iOS": "FR3",
        "iPadOS": "FR3",
        "tvOS": "FR3",
        "android": "FRA3"
      },
      "launchStyle": {
        "watchOS": "modal",
        "macOS": "modal",
        "iOS": "modal",
        "iPadOS": "popover",
        "tvOS": "modal",
        "android": "widget"
      },
      "flowPersistence": {
        "watchOS": "removedAfterProceeding",
        "macOS": "removedAfterProceeding",
        "iOS": "removedAfterProceeding",
        "iPadOS": "removedAfterProceeding",
        "tvOS": "removedAfterProceeding",
        "android": "somethingElse"
      }
    }
  ]
}
```
</details>

<details>
    <summary><b>An implementation that builds on the platform style, but allows using a wildcard `*` to set a default and provide the ability to override as needed.</b></summary>

```json
{
  "schemaVersion": "v0.0.1",
  "sequence": [
    {
      "flowRepresentableName": {
        "*": "FR3",
        "android": "FRA3"
      },
      "launchStyle": {
        "*": "modal",
        "iPadOS": "popover",
        "android": "widget"
      },
      "flowPersistence": {
        "*": "removedAfterProceeding",
        "android": "somethingElse"
      }
    }
  ]
}
```
</details>
