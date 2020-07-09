# NPM cheat sheet

A list of simple but helpful commands for npm

## Prereleasing
* `npm version prerelease --preid=example`: Create a prerelease version with a specific name
* `npm publish --tag example`: Publish current package under a specific tag (nb. Default is `latest`)
* `npm dist-tag ls`: Show all distribution tags for published packages

## Miscellaneous
* `npm ls <package>`: Determine why a particular package is installed

## yarn specific
* `yarn why <package>`: Determine why a particular package is installed
* `yarn cache clean`: Clear the global cache used during package install
