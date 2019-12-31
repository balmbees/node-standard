# Vingle Renovate configuration

A common [Renovate](https://github.com/renovatebot/renovate) configuration for Node.js projects at Vingle.

## Setup

```bash
$ npm install @vingle/renovate-config --save-dev
```

Add the following to `renovate.json`

```json
{
  "extends": ["@vingle"]
}
```


### Node.js specific presets

#### Node.js 8

```json
{
  "extends": ["@vingle", "@vingle:nodejs8"]
}
```

#### Node.js 10

```json
{
  "extends": ["@vingle", "@vingle:nodejs10"]
}
```
#### Node.js 12

```json
{
  "extends": ["@vingle", "@vingle:nodejs12"]
}
```


### AWS Lambda specific presets

For AWS Lambda projects, Use following renovate preset:

```json
{
  "extends": ["@vingle", "@vingle:nodejs8", "@vingle:lambda"]
}
```

### Semantic Commit specific presets

For semantic-release dependent projects, Use following renovate preset:

```json
{
  "extends": ["@vingle", "@vingle:semantic-commit"]
}
```


### Assignee presets

For team-specific projects, Use following renovate preset:

```json
{
  "extends": ["@vingle", "@vingle:assignees:backend"]
}
```

