# Welcome to Restate

Restate is a system for easily building resilient applications using **distributed durable RPC & async/await**.

This repository shows you how to get access to the Restate runtime Docker image

❓ Learn more about Restate from the [Restate documentation](https://docs.restate.dev).

## Prerequisites
- [Docker Engine](https://docs.docker.com/engine/install/) to launch the Restate runtime (not needed for the app implementation itself).
- A GitHub account

## Creating a personal access token
To get started, you first have to [create a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token#creating-a-personal-access-token-classic) (PAT) on GitHub with `read:packages` permission.
This will allow you to access all of Restate's packages.

## Setting up access to the Restate Docker image

To [log into ghcr.io](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry#authenticating-with-a-personal-access-token-classic) you need the previously generated PAT.

```bash
echo $PAT | docker login ghcr.io -u <your-GitHub-user-name> --password-stdin
```

From now on, you can fetch the latest Restate distribution via:

```bash
docker pull ghcr.io/restatedev/restate-dist:latest
```

# Exploring Restate

Check out the following resources for learning more about Restate

* [Documentation](https://docs.restate.dev) to learn more about Restate.
* [Typescript SDK](https://github.com/restatedev/sdk-typescript) to develop Typescript services with Restate.
* [Node template generator](https://github.com/restatedev/node-template-generator) project to develop your own Typescript services.
* [Restate examples](https://github.com/restatedev/examples) showing you Restate in action!
