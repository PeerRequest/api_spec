## Getting started

### Installation

1. Clone the repository.

    ```
    git clone https://github.com/PeerRequest/api_spec
    ```

2. Install the project dependencies.

    ```
    npm install
    ```

3. Edit `openapi.yaml` to fit your API definition. If you’re not familiar with the OpenAPI Specification, read [Getting started with OAS](https://swagger.io/solutions/getting-started-with-oas/) first.

## Useful commands

The project will build, lint, and preview the OpenAPI document from the terminal, with the following commands:

### Build

The command bundles the spec as one `.yaml` file.

```
npm run build
```

The minified document is stored in `_build/openapi.yaml`.

### Test

The command checks if the document follows the OpenAPI 3.0 Specification.

```
npm run test
```

### Preview

The command builds a docs site so that you can view the rendering on your local browser.

```
npm run preview
```

The server starts on http://127.0.0.1:8080.

The site is generated with [ReDoc](https://github.com/Redocly/redoc).

## Workflows

The project uses [GitHub Actions](https://github.com/features/actions) for Continuous Integration (CI).

On every new pull request, the OpenAPI document is linted with [spectral](https://github.com/stoplightio/spectral). If there are changes that introduce errors, the bot will highlight them replying to the pull request.

When the default branch (e.g. `master`) receives an update, a workflow automatically publishes the API reference documentation site to GitHub Pages.

See `.github/workflows` to customize the available workflows. If you don't plan to use GitHub to host your spec or prefer to keep docs private, delete the `.github` folder.
