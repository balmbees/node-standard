# Vingle semantic-release configuration

A common [semantic-release](https://github.com/semantic-release/semantic-release) configuration for TypeScript projects at Vingle.

## Setup

```bash
$ npm install @vingle/semantic-release-config --save-dev
```

Add the following to `.releaserc.json`

```json
{
  "extends": "@vingle/semantic-release-config"
}
```

Add the following to CI Script:

```bash
$ npx semantic-release
```


## Configurations

#### Default

This is commonly used preset.

```json
{
  "extends": "@vingle/semantic-release-config"
}
```


#### Embedded Packages

This is special configuration for embedded packages where package co-located with service.

For example, Media SDK located in Media Service repository, and non-sdk related commits are not using semantic-commits.

In this case, Use this configuration.

```json
{
  "extends": "@vingle/semantic-release-config",
  "successComment": false
}
```

and switch directory to package root before executing semantic-release.

For example:

```bash
$ cd media-sdk
$ npx semantic-release
```
