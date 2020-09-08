# What is a charm?

## Definition

## Different platforms

## Anatomy of a charm
A charm is a bundle of files containing the following:

-   `/hooks` must be a directory holding executables with specific names, that will be invoked by juju at the relevant times. A charm needs to implement at least one hook in order to do anything at all. How to implement hooks is covered more thoroughly in the [Hooks section](https://discourse.juju.is/t/charm-hooks/1040)
-   `/actions` must be a directory holding executables with specific names, which the user may invoke through Juju as desired. See [Actions for the charm author](https://discourse.juju.is/t/actions-for-the-charm-author/1113).
-   `/tests` is an optional directory containing scripts which will be executed in order to ensure that the service works properly. Every executable file on this directory will be executed by `juju test` and the Continuous Integration (CI) tools. See [Writing charm tests](https://discourse.juju.is/t/writing-charm-tests/1130).
- `actions.yaml` specifies charm actions and their schemas, and must be defined if `/actions` is used. See [Actions for the charm author](https://discourse.juju.is/t/actions-for-the-charm-author/1113) for more on creating charm actions.
- `config.yaml` defines service configuration options. [The config.yaml file is descibed more fully here](https://discourse.juju.is/t/creating-config-yaml-and-configuring-charms/1039).
- `icon.svg` is used to identify your charm in the GUI and in the charm store. [See the walkthrough for creating an icon.](https://discourse.juju.is/t/creating-icons-for-charms/1041)
- `README` is made available in the charm store. It should be comprehensible to a reasonably ignorant user.

Above information taken from [here](https://discourse.juju.is/t/components-of-a-charm/1038)

## Charm frameworks
