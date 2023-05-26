# Welcome to Restate

Restate is a system for easily building resilient applications using **distributed durable RPC & async/await**.

This repository shows you how to get access to the Restate runtime Docker image and the Restate npm packages (e.g. Restate's Typescript SDK).

❓ Learn more about Restate from the [Restate documentation](https://github.com/restatedev/documentation).

## Prerequisites
- [NodeJS (and npm)](https://nodejs.org) installed.
- [Docker Engine](https://docs.docker.com/engine/install/) to launch the Restate runtime (not needed for the app implementation itself).
- A GitHub account

## Creating a personal access token
To get started, you first have to [create a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic) (PAT) on GitHub with `read:packages` permission.
This will allow you to access all of Restate's packages.

## Setting up access to the Restate Docker image

To [log into ghcr.io](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic) you need the previously generated PAT.

```bash
echo $PAT | docker login ghcr.io -u USERNAME --password-stdin
```

From now on, you can fetch the latest Restate distribution via:

```bash
docker pull ghcr.io/restatedev/restate-dist:latest
```

## Setting up access to Restate npm packages

To [log into GitHub's npm registry](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry#authenticating-with-a-personal-access-token) you need your username and PAT.

```bash
npm login --scope=restatedev --auth-type=legacy --registry=https://npm.pkg.github.com
```

This will ask for your username and password:

```bash
> Username: USERNAME
> Password: PAT
```

After you have logged in, you can fetch the latest npm packages from `@restatedev`.

# Exploring Restate

Check out the following resources for learning more about Restate

* [Documentation](https://github.com/restatedev/documentation) to learn more about Restate.
* [Typescript SDK](https://github.com/restatedev/sdk-typescript) to develop Typescript services with Restate.
* [Node template generator](https://github.com/restatedev/node-template-generator) project to develop your own Typescript services.
* [Shopping cart example](https://github.com/restatedev/example-shopping-cart-typescript) which demonstrates how to build a web application with Restate.
* [Lambda deployment example](https://github.com/restatedev/example-lambda-ts-greeter) which demonstrates how to deploy your services on [AWS Lambda](https://aws.amazon.com/de/lambda/).
* [Ticket reservation system](https://github.com/restatedev/example-ticket-reservation-system) which illustrate how Restate's keyed-sharding and concurrency guarantees simplify microservice architectures.
