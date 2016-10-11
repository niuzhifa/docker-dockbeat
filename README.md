# Dockerised dockbeat

This is the source for [`redmatter/dockbeat`](https://hub.docker.com/r/redmatter/dockbeat) docker image.

This repackages the prebuilt binaries from [dockbeat repository](https://github.com/Ingensi/dockbeat) and it follows
upstream tags / releases.

## How to use it?

The container does not come with a config file. So you will need to customise [`dockbeat.yml`](dockbeat.yml) before you
get going. Once you have created a customised `dockbeat.yml`, you can run the below command to get going.

    docker run -d \
        -v /var/run/docker.sock:/var/run/docker.sock \
        -v /path/to/config-directory:/etc/dockbeat \
        redmatter/dockbeat

