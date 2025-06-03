<!-- omit in toc -->
## Apio Developement Builds

[![Test](https://github.com/FPGAwars/apio/actions/workflows/test.yml/badge.svg?branch=develop)](https://github.com/FPGAwars/apio/actions/workflows/test.yml)

[![build-all](https://github.com/FPGAwars/apio-dev-builds/actions/workflows/build-all.yaml/badge.svg?branch=main)](https://github.com/FPGAwars/apio-dev-builds/actions/workflows/build-all.yaml)

<!-- Use VCS 'Markdown All In One' extension to update this TOC. -->
- [Background](#background)
- [Installing Apio](#installing-apio)
  - [All supported platforms](#all-supported-platforms)
    - [Using a Python pip package](#using-a-python-pip-package)
  - [Mac OSX (Apple Silicon)](#mac-osx-apple-silicon)
    - [Using an installer](#using-an-installer)
    - [Using a file bundle](#using-a-file-bundle)
  - [Linux (X86 64 bit)](#linux-x86-64-bit)
    - [Using a Debian package](#using-a-debian-package)
    - [Using a file bundle](#using-a-file-bundle-1)
  - [Windows (X86 64 bit)](#windows-x86-64-bit)
    - [Using an installer](#using-an-installer-1)
    - [Using a file bundle](#using-a-file-bundle-2)


## Background

This repository contains the build workflows and the daily releases of the [Apio](https://github.com/FPGAwars/apio), an easy to use FPGA design framework. For installation, see the instructions below.

Apio is currently supported on the following platforms:

| Code          | Description                         |
| :------------ | :---------------------------------- |
| darwin_arm64  | Mac OSX, ARM 64 bit (Apple Silicon) |
| darwin_x86_64 | Mac OSX, x86 64 bit (Intel)         |
| linux_x86_64  | Linux X86 64 bit                    |
| linux_aarch64 | Linux ARM 64 bit                    |
| windows_amd64 | Windows x86 64 bit                  |


[NOTES]
* **To upgrade** an already installed Apio, first uninstall it and then install the new version.
* If you encounter any problem, please **create an issue** in the [Apio's main repository](https://github.com/FPGAwars/apio/issues).

<br>

**TODO:** Add installation instructions darwin_x86_64

**TODO:** Add installation instructions linux_aarch64

<br>

## Installing Apio
----

### All supported platforms

#### Using a Python pip package

This installation method doesn't use a build and instead it simply installs the latest Apio source files as an executable Python Pip package. If you already have Python installed on your system, this may be the easiest way to go. Otherwise, you may consider the self contained installation methods below.

**Install**

1. Run `python --version`` and verify that you have a reasonably recent python version. See Apio's *requires-python* in it's [project file](https://github.com/FPGAwars/apio/blob/develop/pyproject.toml).

2. Install the latest Apio code as a Pip package by running the following command.

```
pip install --force-reinstall -U git+https://github.com/FPGAwars/apio.git@develop#egg=apio
```

3. Run `apio` in a new shell to test the installation.


**Uninstall**

1. Delete the `apio` pip package by running `pip uninstall apio`.

2. Delete the Apio settings directory `.apio` under your home directory.

----
### Mac OSX (Apple Silicon)

#### Using an installer

**Install**

1. Download the installer file **apio-darwin-arm64-[version]-[date]-installer.pkg** from the [latest release](../../releases/latest).

2. Run the following command in the directory where you downloaded the installer file (replace `[version]` and `[date]` with the actual values) this will allow the unsigned installer to run.

```
xattr -d com.apple.quarantine apio-darwin-arm64-[version]-[date]-installer.pkg
```

1. Double click on the installer file and follow the instructions.

2. Run `apio` in a new shell to test the installation.

**Unnstall**

1. Delete the `apio` application from `Applications`.

2. Delete the Apio settings directory `.apio` under your home directory.



#### Using a file bundle


**Install**

1. Download the bundle file **apio-darwin-arm64-[version]-[date]-bundle.zip** from the [latest release](../../releases/latest).

2. Unzip the bundle file. This will create an `apio` directory with the application files.

3. Run the following shell command in the `apio` directory to allow the unsigned files of the Apio app to run.

```
source ./activate
```

4. [Optional] Move the `apio` dir to a place of your choosing.

5. Add the `apio` dir to your `$PATH`.

6. Open a new shell and run `apio` to test the installation.


**Unnstall**

1. Remove the `apio` directory from your `$PATH`

2. Delete the `apio` directory

3. Delete the Apio settings directory `.apio` under your home directory.


----
### Linux (X86 64 bit)

#### Using a Debian package

**Install**

1. Download the debian package file **apio-linux-x86-64-[version]-[date]-debian.deb** from the [latest release](../../releases/latest).

2. Run the following shell command in the the directory where you downloaded the Debian package (replace `[version]` and `[date]` with the actual values) .

```
sudo apt install ./apio-linux-x86-64-[version]-[date]-debian.deb
```

2. Open a new shell and run `apio` to test the installation.

**Unnstall**

1. Run the following command to uninstall the Debian package:

```
sudo apt remove apio
```

2. Delete the Apio settings directory `.apio` under your home directory.



#### Using a file bundle


**Install**

1. Download the bundle file **apio-linux-x86-64-[version]-[date]-bundle.zip** from the [latest release](../../releases/latest).

2. Unzip the bundle file. This will create an `apio` directory with the application files.

3. [Optional] Move the `apio` dir to a place of your choosing.

4. Add the `apio` dir to your `$PATH`.

5. Open a new shell and run `apio` to test the installation.


**Unnstall**

1. Remove the `apio` directory from your `$PATH`

2. Delete the `apio` directory

3. Delete the Apio settings directory `.apio` under your home directory.



-----
### Windows (X86 64 bit)

#### Using an installer


**Install**

1. Download the installer file **apio-windows-amd64-[version]-[date]-installer.exe** from the [latest release](../../releases/latest).

2. Double click on the installer and follow the instructions. If your system complains that the installer is not signed, click **Mofe Info** and the **Run Anyway**.

3. Run `apio` in a new shell to test the installation.


**Unnstall**


1. Remove the `apio` application in windows's `Add or remove programs` settings.

2. Delete the Apio settings directory `.apio` under your home directory.

#### Using a file bundle

**Install**

1. Download the bundle file **apio-windows-amd64-[version]-[date]-bundle.zip** from the [latest release](../../releases/latest).

2. Unzip the bundle file. This will create an `apio` directory with the application files.
  
3. [Optional] Move the `apio` dir to a place of your choosing.

4. Add the `apio` dir to your `%PATH%`.

5. Open a new command window and run `apio` to test the installation.


**Unnstall**

1. Remove the `apio` directory from your `%PATH%`

2. Delete the `apio` directory

3. Delete the Apio settings directory `.apio` under your home directory.

