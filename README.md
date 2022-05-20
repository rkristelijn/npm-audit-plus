# NPM Audit+

**NPM Audit+** is a wrapper around NPM's [built-in audit tool](https://docs.npmjs.com/cli/audit). It adds the following functionality:

- Ignore particular advisories
- Specify a project to audit
- Output audit result as JUnit XML, compatible with many CI systems

## Installation

Install globally:

```sh
npm install -g npm-audit-plus
```

or install locally:

```sh
npm install npm-audit-plus
```

Either works!

## Usage

```sh
npm-audit-plus --ignore=123,456 --xml             # If installed globally
$(npm bin)/npm-audit-plus --ignore=123,456 --xml  # If installed locally
```

For more documentation on NPM Audit+'s flags, run

```sh
npm-audit-plus --help             # If installed globally
$(npm bin)/npm-audit-plus --help  # If installed locally
```

Other usage

```sh
npx npm-audit-plus --production # Ignore vulnerabilities in devDependencies
```

```sh
npx npm-audit-plus --audit-level=high # Only exit with code non-zero on high and critical
```
