# setup-steamcmd

[![Integration test status](https://github.com/andriivitiv/setup-steamcmd/workflows/Integration%20test/badge.svg)](https://github.com/andriivitiv/setup-steamcmd/actions)
[![License: MIT](https://img.shields.io/github/license/andriivitiv/setup-steamcmd?label=License)](LICENSE)

A GitHub Action that installs and configures the Steam Console Client (SteamCMD) for use in workflows.

# Usage

Example of installing SteamCMD and updating an app:

```yaml
steps:
- name: Setup steamcmd
  uses: andriivitiv/setup-steamcmd@v1

- name: Update app
  run: steamcmd +login anonymous +app_update 480 validate +quit
```

More information about SteamCMD can be found in the [official wiki](https://developer.valvesoftware.com/wiki/SteamCMD).

# Outputs

| name       | description                                   |
|------------|-----------------------------------------------|
| directory  | Directory where SteamCMD was installed.       |
| executable | Path to `steamcmd.sh` or `steamcmd.exe` file. |
