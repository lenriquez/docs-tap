# Install Services Toolkit

This document describes how to install Services Toolkit
from the Tanzu Application Platform package repository.

>**Note:** Use the instructions on this page if you do not want to use a profile to install packages.
Both the full and light profiles include Services Toolkit.
For more information about profiles, see [Installing the Tanzu Application Platform Package and Profiles](../install.md).

## <a id='prereqs'></a>Prerequisites

Before installing Services Toolkit:

- Complete all prerequisites to install Tanzu Application Platform. For more information, see [Prerequisites](../prerequisites.md).

## <a id='install-services-toolkit'></a> Install Services Toolkit

To install Services Toolkit:

1. See what versions of Services Toolkit are available to install by running:

    ```
    tanzu package available list -n tap-install services-toolkit.tanzu.vmware.com
    ```

    For example:

    ```
    $ tanzu package available list -n tap-install services-toolkit.tanzu.vmware.com
    - Retrieving package versions for services-toolkit.tanzu.vmware.com...
      NAME                               VERSION           RELEASED-AT
      services-toolkit.tanzu.vmware.com  0.5.0             2021-10-18T09:45:46Z
    ```

1. Install Services Toolkit by running:

    ```
    tanzu package install services-toolkit -n tap-install -p services-toolkit.tanzu.vmware.com -v 0.5.0
    ```

1. Verify that the package installed by running:

    ```
    tanzu package installed get services-toolkit -n tap-install
    ```

    and checking that the `STATUS` value is `Reconcile succeeded`

    For example:

    ```
    $ tanzu package installed get services-toolkit -n tap-install
    | Retrieving installation details for services-toolkit...
    NAME:                    services-toolkit
    PACKAGE-NAME:            services-toolkit.tanzu.vmware.com
    PACKAGE-VERSION:         0.5.0
    STATUS:                  Reconcile succeeded
    CONDITIONS:              [{ReconcileSucceeded True  }]
    USEFUL-ERROR-MESSAGE:
    ```
    
