# Overview

The default plugin repository for [Eva](https://github.com/edouardpoitras/eva).

The `plugins.csv` file in this repo is effectively the list of all plugins that Eva can see.

When Eva boots up, it attempts to enable all the plugins specified in it's configuration file.
If a plugin is not found locally, Eva will fetch the plugin based on it's entry in the `plugins.csv` file (if found).

The file is also parsed by the [Web UI Plugins](https://github.com/edouardpoitras/eva-web-ui-plugins) plugin to list the available plugins for the user to download in the Web UI.

If you wish to add your plugin to the default plugin repository, create a [pull request](https://github.com/edouardpoitras/eva-plugin-repository/compare) with your added entry in plugins.csv file.

Please keep the file in alphabetical order.

## Custom Plugin Repository

Users can specify a different plugin repository by setting a value in `eva.conf`:

    [eva]
    # The git-accessible repo that holds all the available Eva plugins for download.
    #plugin_repository = 'https://github.com/edouardpoitras/eva-plugin-repository.git'
    plugin_repository = 'https://my.gitlab.com/me/custom-plugin-repository.git'
