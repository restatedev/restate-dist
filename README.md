# Welcome to Restate; the easy way of building modern distributed applications

In order to get started, you first have to [create a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic) (PAT) with `read:packages` permissions.
This will allow you to access the Github package registry.

## Container registry

In order to [log into ghcr.io](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic) you need the previously generated PAT.

```bash
$ echo $PAT | docker login ghcr.io -u USERNAME --password-stdin
```

From now on, you can fetch the latest Restate distribution via:

```bash
$ docker pull ghcr.io/restatedev/restate-dist:latest
```

## NPM registry

In order to [log into Github's npm registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry#authenticating-with-a-personal-access-token) you need your username and PAT.

```bash
$ npm login --scope=restatedev --auth-type=legacy --registry=https://npm.pkg.github.com

> Username: USERNAME
> Password: PAT
```

After you have logged in, you can fetch the latest npm packages from the `@restatedev`.

# Exploring Restate

Check out the following resources for learning more about Restate

* [Typescript SDK](https://github.com/restatedev/sdk-typescript) to develop Typescript services with Restate
* [Node template](https://github.com/restatedev/node-template) project to develop your own Typescript services
* [Shopping cart example](https://github.com/restatedev/example-shopping-cart-typescript) which demonstrates how to build a web application with Restate
* [Lambda deployment example](https://github.com/restatedev/example-lambda-ts-greeter) which demonstrates how to deploy your services on [AWS Lambda](https://aws.amazon.com/de/lambda/).
