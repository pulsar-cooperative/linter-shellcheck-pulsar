# linter-shellcheck-pulsar

<!-- Pulsar Cooperative Package Repository Template, place underneath the first h1 heading in the original readme -->

> [!NOTE]
> This package was originally created by <ORIGINAL_AUTHORS_NAME> and has now been forked under the [`pulsar-cooperative`](https://github.com/pulsar-cooperative) organization.
> By forking this package we hope to allow new maintainers to work on this package as needed, without being limited by its previous [archived/unmaintained] status, helping to ensure this package stays up to date and functional for as long as possible without the huge responsibility implied by forking and maintaining this under a personal account.
>
> For more info on the Pulsar Cooperative initiative please read [the documentation](https://github.com/pulsar-cooperative/.github/blob/main/CONTRIBUTING.md).

<!-- Original Readme to follow -->

This linter plugin for [Linter][linter] provides an interface to
[shellcheck][shellcheck]. It will be used with files that have the "Shell"
syntax.

## Installation

Linter package must be installed in order to use this plugin. If Linter is not
installed, please follow the instructions [here][linter].

### `shellcheck` installation

Before using this plugin, you must ensure that `shellcheck` is installed on
your system. To install `shellcheck`, follow the guide on
[shellcheck github][shellcheck]

### Plugin installation

```ShellSession
ppm install linter-shellcheck-pulsar
```

## Settings

You can configure linter-shellcheck-pulsar through Pulsar's Settings menu. If you
instead prefer editing the configuration by hand you can get to that by editing
`~/.atom/config.cson` (choose Open Your Config in Pulsar menu). The settings
available are:

-   `shellcheckExecutablePath`: The full path to the `shellcheck` executable.
    Run `which shellcheck` to find where it is installed on your system.

-   `userParameters`: Any additional executable parameters to pass to
    `shellcheck` when linting your files.

-   `enableNotice`: Include lesser-importance ShellCheck messages
    (default: false).

-   `useProjectCwd`: Controls whether the paths used by ShellCheck's
    [`source=`](https://github.com/koalaman/shellcheck/wiki/Directive#source)
    directive are relative to the project root or the file (default: false, for
    file-relative)

    -   If true, ShellCheck's working directory
        will be the project's root directory.  Any `source=` directives will be
        interpreted relative to the project root.

    -   Otherwise, ShellCheck will run relative to the file's directory,
        making `source=` directives file-relative.

[linter]: https://github.com/atom-community/linter "Linter"
[shellcheck]: https://github.com/koalaman/shellcheck "ShellCheck"
