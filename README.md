# Discogs with ![Qlik logo](./src/img/Qlik_Logo.svg) Mashup

[![License](https://img.shields.io/badge/license-ISC-blue.svg)](https://opensource.org/licenses/ISC)

This is a [Qlik Sense mashup](https://qlik.dev/embed/foundational-knowledge/web-app-mashup-intro/) with Embed Objects. [Check limitation](https://qlik.dev/extend/extend-qlik-visualizations/supported-charts/) to object with Qlik Embed html web tag.

## Getting Started

Before we get started, you'll need to install Node and npm (or Yarn).

### Contributing

Add .env file with parameter

```.env
PROJECT_NAME="Qlik & Discogs Mashup"
TENANT_URL="https://<tenant>.eu.qlikcloud.com"
APP_ID="<app_id>"
WEB_INTEGRATION_ID="<web_integration_id>"
```

Change in index.html file

```js
    <script
      crossorigin="anonymous"
      src="https://cdn.jsdelivr.net/npm/@qlik/embed-web-components@1/dist/index.min.js"
      data-host="https://<tenant>.eu.qlikcloud.com"
      data-web-integration-id="<web_integration_id>"
      data-cross-site-cookies="false"
      data-auto-redirect="true"
    ></script>
```

#### Managing web integrations

You can create web integrations to add origins that are allowlisted to access the tenant. The web integration containing the allowlist is connected to an ID used in for example a mashup that is connecting to your tenant. When a request arrives, Qlik Cloud confirms that the request derives from an allowlisted domain and then approves the request, else not.

source : https://help.qlik.com/en-US/cloud-services/Subsystems/Hub/Content/Sense_Hub/Admin/mc-adminster-web-integrations.htm

## Installation Qlik mashup

Install package

```bash
npm install
```

Start a local server using:

```bash
npm run server
```

Start a dev on local machine using:

```bash
npm run dev
```

Check version npm package on package.json

```bash
npx npm-check-updates -u
```
