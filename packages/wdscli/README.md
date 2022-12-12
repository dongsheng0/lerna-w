oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g wdscli
$ wdscli COMMAND
running command...
$ wdscli (--version)
wdscli/0.0.0 darwin-x64 node-v16.18.0
$ wdscli --help [COMMAND]
USAGE
  $ wdscli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`wdscli hello PERSON`](#wdscli-hello-person)
* [`wdscli hello world`](#wdscli-hello-world)
* [`wdscli help [COMMAND]`](#wdscli-help-command)
* [`wdscli plugins`](#wdscli-plugins)
* [`wdscli plugins:install PLUGIN...`](#wdscli-pluginsinstall-plugin)
* [`wdscli plugins:inspect PLUGIN...`](#wdscli-pluginsinspect-plugin)
* [`wdscli plugins:install PLUGIN...`](#wdscli-pluginsinstall-plugin-1)
* [`wdscli plugins:link PLUGIN`](#wdscli-pluginslink-plugin)
* [`wdscli plugins:uninstall PLUGIN...`](#wdscli-pluginsuninstall-plugin)
* [`wdscli plugins:uninstall PLUGIN...`](#wdscli-pluginsuninstall-plugin-1)
* [`wdscli plugins:uninstall PLUGIN...`](#wdscli-pluginsuninstall-plugin-2)
* [`wdscli plugins update`](#wdscli-plugins-update)

## `wdscli hello PERSON`

Say hello

```
USAGE
  $ wdscli hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Who is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/packages/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `wdscli hello world`

Say hello world

```
USAGE
  $ wdscli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ wdscli hello world
  hello world! (./src/commands/hello/world.ts)
```

## `wdscli help [COMMAND]`

Display help for wdscli.

```
USAGE
  $ wdscli help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for wdscli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.20/src/commands/help.ts)_

## `wdscli plugins`

List installed plugins.

```
USAGE
  $ wdscli plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ wdscli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.1.8/src/commands/plugins/index.ts)_

## `wdscli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ wdscli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ wdscli plugins add

EXAMPLES
  $ wdscli plugins:install myplugin 

  $ wdscli plugins:install https://github.com/someuser/someplugin

  $ wdscli plugins:install someuser/someplugin
```

## `wdscli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ wdscli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ wdscli plugins:inspect myplugin
```

## `wdscli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ wdscli plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.
  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.


ALIASES
  $ wdscli plugins add

EXAMPLES
  $ wdscli plugins:install myplugin 

  $ wdscli plugins:install https://github.com/someuser/someplugin

  $ wdscli plugins:install someuser/someplugin
```

## `wdscli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ wdscli plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.
  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.


EXAMPLES
  $ wdscli plugins:link myplugin
```

## `wdscli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ wdscli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ wdscli plugins unlink
  $ wdscli plugins remove
```

## `wdscli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ wdscli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ wdscli plugins unlink
  $ wdscli plugins remove
```

## `wdscli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ wdscli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ wdscli plugins unlink
  $ wdscli plugins remove
```

## `wdscli plugins update`

Update installed plugins.

```
USAGE
  $ wdscli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
