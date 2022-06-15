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
$ npm install -g start-cli
$ start-cli COMMAND
running command...
$ start-cli (--version)
start-cli/0.0.0 linux-x64 node-v16.15.1
$ start-cli --help [COMMAND]
USAGE
  $ start-cli COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`start-cli hello PERSON`](#start-cli-hello-person)
* [`start-cli hello world`](#start-cli-hello-world)
* [`start-cli help [COMMAND]`](#start-cli-help-command)
* [`start-cli plugins`](#start-cli-plugins)
* [`start-cli plugins:install PLUGIN...`](#start-cli-pluginsinstall-plugin)
* [`start-cli plugins:inspect PLUGIN...`](#start-cli-pluginsinspect-plugin)
* [`start-cli plugins:install PLUGIN...`](#start-cli-pluginsinstall-plugin-1)
* [`start-cli plugins:link PLUGIN`](#start-cli-pluginslink-plugin)
* [`start-cli plugins:uninstall PLUGIN...`](#start-cli-pluginsuninstall-plugin)
* [`start-cli plugins:uninstall PLUGIN...`](#start-cli-pluginsuninstall-plugin-1)
* [`start-cli plugins:uninstall PLUGIN...`](#start-cli-pluginsuninstall-plugin-2)
* [`start-cli plugins update`](#start-cli-plugins-update)

## `start-cli hello PERSON`

Say hello

```
USAGE
  $ start-cli hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/luangazin/start-cli/blob/v0.0.0/dist/commands/hello/index.ts)_

## `start-cli hello world`

Say hello world

```
USAGE
  $ start-cli hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `start-cli help [COMMAND]`

Display help for start-cli.

```
USAGE
  $ start-cli help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for start-cli.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `start-cli plugins`

List installed plugins.

```
USAGE
  $ start-cli plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ start-cli plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `start-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ start-cli plugins:install PLUGIN...

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
  $ start-cli plugins add

EXAMPLES
  $ start-cli plugins:install myplugin 

  $ start-cli plugins:install https://github.com/someuser/someplugin

  $ start-cli plugins:install someuser/someplugin
```

## `start-cli plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ start-cli plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ start-cli plugins:inspect myplugin
```

## `start-cli plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ start-cli plugins:install PLUGIN...

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
  $ start-cli plugins add

EXAMPLES
  $ start-cli plugins:install myplugin 

  $ start-cli plugins:install https://github.com/someuser/someplugin

  $ start-cli plugins:install someuser/someplugin
```

## `start-cli plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ start-cli plugins:link PLUGIN

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
  $ start-cli plugins:link myplugin
```

## `start-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ start-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ start-cli plugins unlink
  $ start-cli plugins remove
```

## `start-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ start-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ start-cli plugins unlink
  $ start-cli plugins remove
```

## `start-cli plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ start-cli plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ start-cli plugins unlink
  $ start-cli plugins remove
```

## `start-cli plugins update`

Update installed plugins.

```
USAGE
  $ start-cli plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
