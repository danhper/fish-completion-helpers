# fish-completions-helpers

Helper functions to make subcommands completions easier with fish.

## Installation

## Using fundle (recommended)

Add

```
fundle plugin 'tuvistavie/fish-fastdir'
```

to your `config.fish` and run `fundle install`.

## Manual

Add the two files in [the functions directory](https://github.com/tuvistavie/fish-completions-helpers/tree/master/functions) in `~/.config/fish/functions`.

## Usage

For the program main commands, add `__fish_prog_needs_command CMD_NAME` to complete condition (`-n` flag). Example:

```
complete -f -c cmd -n '__fish_prog_needs_command cmd' -a start -d "start my cmd"
```

For the program subcommands, add `__fish_prog_using_command SUBCMD` to complete condition (`-n` flag). Example:

```
complete -f -c cmd -n '__fish_prog_using_command start' -l daemon "start as daemon"
```
