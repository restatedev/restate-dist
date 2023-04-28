# Releasing the Restate distribution

In order to release the Restate distribution, you first have to create a release in [restatedev/restate](https://github.com/restatedev/restate).

Next you can manually trigger the [Export Restate release workflow](./.github/workflows/export_restate_release.yml) by provding the release tag of the **restatedev/restate** release.
This workflow will first check that a release with the provided tag exists in [restatedev/restate](https://github.com/restatedev/restate).
Next, the workflow will update the [Dockerfile](./docker/Dockerfile) to point to the released `ghcr.io/restatedev/restate` container image and create a tag for the release.
As a result of creating this tag, the [docker image workflow](./.github/workflow/docker.yml) and the [release workflow](./.github/workflow/docker.yml) will be started.
The docker image workflow builds and publishes the `ghcr.io/restatedev/restate-dist` image.
The release workflow will create a draft release with all `restate-cli-*.zip` assets from the **restatedev/restate** release.

In order to finish the release, you have to go the release page and publish the release draft.

If you don't want to automatically export the Restate release via the export Restate release workflow, then you can manually update the `Dockerfile` to point to the correct Restate container image and create then push a tag of the form `vX.Y.Z`. This will build the Docker image as well as creating a draft release for this tag.
