# API Endpoints Documentation

## Overview

This repository (`actionanand/json-server`) serves as a mock API server using JSON files hosted on GitHub. The relative API paths correspond to JSON files stored in the `db/` directory of the repository. These files can be accessed via their absolute raw URLs for direct consumption in applications, such as frontend projects or testing environments.

- **Repository**: `actionanand/json-server`
- **Branch**: `main`
- **GitHub Account**: `actionanand`
- **Base Raw URL**: `https://raw.githubusercontent.com/actionanand/json-server/main/`

## Relationship Between GitHub and Raw URLs

GitHub provides a web interface to view files, while raw URLs allow direct access to the file content (e.g., for API calls or downloads). The mapping is as follows:

- **GitHub URL Format**: `https://github.com/{account}/{repo}/blob/{branch}/{path}`
- **Raw URL Format**: `https://raw.githubusercontent.com/{account}/{repo}/{branch}/{path}`

To convert a GitHub URL to a raw URL:
1. Replace `github.com` with `raw.githubusercontent.com`.
2. Remove `/blob` from the path.

Example:
- GitHub: `https://github.com/actionanand/json-server/blob/main/db/api/arblogz/v1/daily-status.json`
- Raw: `https://raw.githubusercontent.com/actionanand/json-server/main/db/api/arblogz/v1/daily-status.json`

## API Endpoints

The following table lists the relative API paths, their absolute raw URLs, and brief notes on their purpose (based on file names and structure). These are JSON files that can be fetched via HTTP GET requests.

| Relative Path | Absolute Raw URL | Description |
|---------------|------------------|-------------|
| `db/api/arblogz/v1/daily-status.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/api/arblogz/v1/daily-status.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/api/arblogz/v1/daily-status.json) | Likely contains daily status data for an "arblogz" service or module, version 1. |
| `db/api/quiz/questions.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/api/quiz/questions.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/api/quiz/questions.json) | Quiz questions data, possibly for a quiz application. |
| `db/api/quiz/dumbs/cssAndHtml.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/api/quiz/dumbs/cssAndHtml.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/api/quiz/dumbs/cssAndHtml.json) | Dumb (simple) quiz questions related to CSS and HTML. |
| `db/api/angular-js/rough-work/rules.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/api/angular-js/rough-work/rules.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/api/angular-js/rough-work/rules.json) | Rules or configuration for Angular.js rough work or experiments. |
| `db/api/ng-dev-testing/library.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/api/ng-dev-testing/library.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/api/ng-dev-testing/library.json) | Library data for Angular development testing. |
| `db/json/mat-table.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/json/mat-table.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/json/mat-table.json) | Data for a Material Table (likely Angular Material) component. |
| `db/json/single-spa-demo-root-config/importmap.json` | [https://raw.githubusercontent.com/actionanand/json-server/main/db/json/single-spa-demo-root-config/importmap.json](https://raw.githubusercontent.com/actionanand/json-server/main/db/json/single-spa-demo-root-config/importmap.json) | Import map configuration for a Single-SPA demo root config. |

## Usage

- **Fetching Data**: Use the absolute raw URLs in your application to fetch JSON data. For example, in JavaScript:  
  ```javascript
  fetch('https://raw.githubusercontent.com/actionanand/json-server/main/db/api/arblogz/v1/daily-status.json')
    .then(response => response.json())
    .then(data => console.log(data));
  ```
- **CORS Considerations**: Raw GitHub URLs may have CORS restrictions in browsers. For production, consider hosting these files on a proper API server or using a proxy.
- **Updates**: Files are hosted on GitHub, so changes to the repository will reflect in these URLs. Always check the repository for the latest versions.
