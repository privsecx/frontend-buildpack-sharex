# Frontend Buildpack

1. Builds a frontend (yarn build)
1. Copies it into a target location on the server

## Usage

Set environment variables to paths relative to the monorepo root, eg:

```sh
FRONTEND_BUILDPACK_JS_APP=path/to/js-app
FRONTEND_BUILDPACK_JS_ROUTE=url-route-to-client
FRONTEND_BUILDPACK_RAILS_APP=path/to/rails-app/public/subdir
```

This buildpack must come ***before*** any buildpack that removes the JS app directory.
