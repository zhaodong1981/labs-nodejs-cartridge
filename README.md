# Openshift Labs Node.JS

## Usage

Create an app using the latest LTS version 4 (https://semver.io/node/resolve/4):
`rhc create-app <app name> http://nodecartridge-dongrht.rhcloud.com/manifest/LTS-4`

What this cartridge provides out of the box
---
1. **node.js** ([latest LTS](https://semver.io/node/resolve/4) currently 4.6.0)
2. **npm** (latest stable currently 2.15.9)
3. **grunt**
4. **bower**

What this cartridge does out of the box
---
*Not much.*

1. Installs node.js (version specified by `$OPENSHIFT_NODEJS_VERSION` and resolved by [semver.io](https://semver.io))
2. Installs grunt, bower, and forever globally (specified by `$OPENSHIFT_NPM_GLOBALS`)
3. Allows the user to manually install required dependencies (in a `build` [action_hook](http://openshift.github.io/documentation/oo_user_guide.html#action-hooks))
4. Runs `npm start` if `package.json` is found in repo directory (log is written to `$OPENSHIFT_NODEJS_LOG_DIR`)

Thanks to all!
---
These repos helped out a ton while developing this cartridge.
1. [engineersamuel/openshift-origin-cartridge-nodejs](https://github.com/engineersamuel/openshift-origin-cartridge-nodejs)
2. [wshearn/openshift-origin-cartridge-nodejs](https://github.com/wshearn/openshift-origin-cartridge-nodejs)
3. [ramr/nodejs-custom-version-openshift](https://github.com/ramr/nodejs-custom-version-openshift)
4. [heroku/heroku-buildpack-nodejs](https://github.com/heroku/heroku-buildpack-nodejs)
5. [connyay/openshift-node-diy](https://github.com/connyay/openshift-node-diy)
