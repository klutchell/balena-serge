# balena-serge

A chat interface based on llama.cpp for running Alpaca models.

Entirely self-hosted, no API keys needed. Fits on 4GB of RAM and runs on the CPU.

You can read more on the [official project README](https://github.com/serge-chat/serge).

## Hardware required

LLaMA will just crash if you don't have enough available memory for your model.

- 7B requires about 4.5GB of free RAM
- 13B requires about 12GB free
- 30B requires about 20GB free

I've tested on Intel NUC, but any `amd64` or `aarch64` device with at least 5GB of memory should work!

In theory Raspberry Pi 4 8GB model should work but I haven't tried it myself!

## Getting Started

You can one-click-deploy this project to balena using the button below:

[![deploy button](https://balena.io/deploy.svg)](https://dashboard.balena-cloud.com/deploy?repoUrl=https://github.com/klutchell/balena-serge)

## Manual Deployment

Alternatively, deployment can be carried out by manually creating a [balenaCloud account](https://dashboard.balena-cloud.com) and application, flashing a device,
downloading the project and pushing it via the [balena CLI](https://github.com/balena-io/balena-cli).

### Environment Variables

| Name | Default | Purpose                                                                                                                                 |
| ---- | ------- | --------------------------------------------------------------------------------------------------------------------------------------- |
| `TZ` | `UTC`   | The timezone in your location. Find a [list of all timezone values here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones). |

## Usage

Once your device joins the fleet you'll need to allow some time for it to download the application containers.

When it's done you should be able to access the app on port 80 of the device.

You can read more on the [official project README](https://github.com/serge-chat/serge).

## Extras

### Tailscale

Included is a [Tailscale block](https://github.com/klutchell/balena-tailscale) in order to access your app from anywhere!

## Contributing

Please open an issue or submit a pull request with any features, fixes, or changes.
