# bsp-orangepi-5-plus

Board support for the Orange Pi 5 Plus (RK3588 SBC, mainline kernel)

## Using this extension

`bsp-orangepi-5-plus` is an [Avocado](https://avocadolinux.org) extension — a reusable fragment of
build- and runtime-configuration that you compose into your own Avocado project. To use it,
declare it as a package-sourced extension in your `avocado.yaml` and add it to a runtime:

```yaml
extensions:
  avocado-bsp-orangepi-5-plus:
    source:
      type: package
      version: "*"        # or pin an exact version

runtimes:
  my-runtime:
    extensions:
      - avocado-bsp-orangepi-5-plus
```

Then `avocado build`. The extension's config is fetched from your target's package feed
and merged into your project at build time.
