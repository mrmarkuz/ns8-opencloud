# ns8-opencloud

[OpenCloud](https://opencloud.eu) is the Heinlein Group's file sharing & collaboration solution.

## Install

Install via Software center:

  - Add a Software repository pointing to `https://repo.mrmarkuz.com/ns8/updates/`, check out the [repo webpage](https://repo.mrmarkuz.com) how to do it.

Install from CLI:

    add-module add-module ghcr.io/mrmarkuz/opencloud:1.0.1

## Configure

Set the FQDN.

If you don't use a valid certificate following configuration needs to be set, in this example it is set for instance opencloud1:

    runagent -m opencloud1 bash -c "grep -q OC_INSECURE environment || echo OC_INSECURE=true >> environment"

## Uninstall

To uninstall the instance:

    remove-module --no-preserve opencloud1

