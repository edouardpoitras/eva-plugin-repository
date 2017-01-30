# Overview

The default plugin repository for [Eva](https://github.com/edouardpoitras/eva).

The `plugins.csv` file in this repo is effectively the list of all plugins that Eva can see.

When Eva boots up, it attempts to enable all the plugins specified in it's configuration file.
If a plugin is not found locally, Eva will fetch the plugin based on it's entry in the `plugins.csv` file (if found).

The file is also parsed by the [Web UI Plugins](https://github.com/edouardpoitras/eva-web-ui-plugins) plugin to list the available plugins for the user to download in the Web UI.

If you wish to add your plugin to the default plugin repository, create a [pull request](https://github.com/edouardpoitras/eva-plugin-repository/compare) with your added entry in plugins.csv file.

Please keep the file in alphabetical order.

## Plugin Developers

By default, Eva will clone new plugins in the following directory: `~/eva/plugins`

This can be configured in `eva.conf`:

    [eva]
    # The local directory holding all existing (and downloaded) plugins.
    plugin_directory = '~/eva/plugins'

Developers can go directly into that directory to create new plugins, code, and make changes to existing plugins.

Your plugins don't need to be git repositories, but they will not be able to be updated by the [Updater](https://github.com/edouardpoitras/eva-updater) and [Web UI Updater](https://github.com/edouardpoitras/eva-web-ui-updater) plugins if they are not git repositories.

See the [plugin development guide](https://github.com/edouardpoitras/eva/blob/master) for more information on creating your own Eva plugins.

## Private Plugins

You can easily create new custom plugins by simply dropping them in the configured `plugin_directory` and enabling them through the Eva configuration file or the Web UI.

However, we always appreciate contributions and new plugin submissions to the default public repository. If you made Eva better through a private plugin, consider sharing the code.

We understand that it's more difficult to make a plugin for a public repository than it is to make it for oneself. If you feel intimidated sharing your code, don't know how to go about it, or think your plugin is too specialized, let us know. There's a good chance we can make your plugin (even more) awesome. We'd love to help you contribute and grow Eva's list of plugins.

## Custom Plugin Repository

Users can specify a different plugin repository by setting a value in `eva.conf`:

    [eva]
    # The git-accessible repo that holds all the available Eva plugins for download.
    #plugin_repository = 'https://github.com/edouardpoitras/eva-plugin-repository.git'
    plugin_repository = 'https://my.gitlab.com/me/custom-plugin-repository.git'
