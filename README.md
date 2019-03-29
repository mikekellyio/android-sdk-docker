# android-sdk

This builds a docker image with Android SDK already loaded on it for CI use in other projects.

The included `gitlab-ci.yml` file can be used as a template to kickstart using CI on android projects.

**Usage**

1. Install Docker (https://docs.docker.com/install/)
2. [Linux only] Install Docker Compose (https://docs.docker.com/compose/install/)
3. Build image

```
docker-compose build
```

4. Save image to file for installation elsewhere.

```
docker save -o android-sdk.docker android-sdk:latest
```

5. Transfer the file to where it is needed and install using:

```
docker load << android-sdk.docker
```
