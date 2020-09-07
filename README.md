![Node.js CI](https://github.com/digitalroute/jest-jenkins-reporter/workflows/Node.js%20CI/badge.svg?branch=master)

# jest-jenkins-reporter

A plugin that integrates jest test results into Jenkins.

## Installation

```bash
$ npm install --save-dev @digitalroute/jest-jenkins-reporter
# or
$ yarn add @digitalroute/jest-jenkins-reporter --dev
```

## Usage

Configuring `package.json`

Add jest test result processor, here is jest-jenkins-reporter. If you want to use your self processor, you can replace "jest-jenkins-reporter".

```jsonc
// package.json
"jest": {
    // ...
    "testResultsProcessor": "@digitalroute/jest-jenkins-reporter"
}
```

Reporter file config:

```jsonc
// package.json
"jestSonar": {
    "reportPath": "reports",
    "reportFile": "report.xml",
    "indent": 4
}
```

* `reportPath`: Report file generation path.
* `reportFile`: Report file name.
* `indent`: XML file indentation space number.

Test script:

```bash
"test-jenkins": "NODE_ENV=test jest --colors"
```

## License

MIT
