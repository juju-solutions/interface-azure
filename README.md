# Overview

This layer encapsulates the `azure-integration` interface communciation
protocol and provides an API for charms on either side of relations using this
interface.

## Usage

In your charm's `layer.yaml`, ensure that `interface:azure-integration` is
included in the `includes` section:

```yaml
includes: ['layer:basic', 'interface:azure-integration']
```

And in your charm's `metadata.yaml`, ensure that a relation endpoint is defined
using the `azure-integration` interface protocol:

```yaml
requires:
  azure:
    interface: azure-integration
```

For documentation on how to use the API for this interface, see:

* [Requires API documentation](docs/requires.md)
* [Provides API documentation](docs/provides.md) (this will only be used by the azure-integrator charm)
