# NestJS Serverless Monorepo Example

Example integrated NX monorepo with two NestJS apps served locally and deployed via Serverless Framework.

## Setup
1. `npm ci`
2. Update `provider.profile` in `serverless.base.yml` from `default` if necessary for deploys.

## Local Dev
1. `nx run-many --target=serve`
   1. `https://localhost:3000/dev/test/`
   2. `https://localhost:3001/dev/test/`

## Deploy
1. `nx run-many --target=deploy`

## Notes
* The default `serve` target in `project.json` has been updated to use `serverless offline`.
* A `deploy` target was added.
* Several packages were ignored via `custom.bundle.ignorePackages` in `serverless.base.yml` for it to build successfully. This [thread](https://github.com/nestjs/nest/issues/1706) provides background.
