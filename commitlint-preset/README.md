# Vingle commitlint preset

A common commitlint preset for TypeScript projects at Vingle.

## IMPORTANT NOTE

This preset requires global npm dependency. Make sure commitizen is installed: 

```bash
$ npm install commitizen -g
```

## Setup

```bash
$ npm install @vingle/commitlint-preset husky --save-dev
```

Add the following to `package.json`

```json
{
  "config": {
    "commitizen": {
      "path": "cz-conventional-changelog"
    }
  },
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS"
    }
  },
  "commitlint": {
    "extends": [
      "@vingle/commitlint-preset"
    ]
  }
}
```
