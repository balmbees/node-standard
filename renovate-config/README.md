# Vingle Renovate configuration

A common Renovate configuration for Node.js projects at Vingle.

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

```json
{
  "extends": ["@vingle", "@vingle/nodejs8"]
}
``` 


### AWS Lambda specific presets

For AWS Lambda projects, Use following renovate preset:

```json
{
  "extends": ["@vingle", "@vingle:nodejs8", "@vingle:lambda"]
}
```

