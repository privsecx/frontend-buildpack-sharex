# Frontend Buildpack

1. Builds a frontend (yarn build)
1. Copies it into a target location on the server

## Usage

Set environment variables to paths relative to the monorepo root, eg:

```sh
FRONTEND_BUILDPACK_SOURCE_DIR=path/to/js-app
FRONTEND_BUILDPACK_TARGET_DIR=path/to/rails-app/public/subdir
```

This buildpack must come ***before*** any buildpack that removes the source directory.
