# Packer

**Contents** [TL;DR] | [Overview] | [Getting started] | [Usage] | [Next steps] | [Contributing] | [Resources]

This repository contains common [Packer] helper tools and sample templates for [Docker], [IIS], [SQL Server] and [Visual Studio] on [Windows] and [Ubuntu], building virtual machine images and [Vagrant] boxes for [VirtualBox], [Hyper-V], [Azure] and [AWS], provisioned with [Chef].

## TL;DR

- [Vagrant boxes] ready to use for virtualizing hosting and development scenarios.
- [Virtual workstations] for automating the configuration of your development environments.
- Blogs with an overview of the [why][BlogWhy], [how][BlogHow] and what of Packer.

[TL;DR]: #tldr

## Overview

**Contents** [Operating systems] | [Hosting] | [Development]

> **Note** This section covers the details of the published [Vagrant boxes] this repository builds. See the [Getting started] section to build your own virtual machine images. See [virtual workstations] for samples of automating the configuration of your development environments using them and [these][BlogWhy] [blogs][BlogHow] for more background and motivation.

This repository contains [Packer] sample template for the following virtualization scenarios:

- [Operating systems] for generic experiments with [Windows] and [Ubuntu].
- [Hosting] using [Docker], [IIS] and [SQL Server].
- [Development] using [Visual Studio].

The virtual machine images and [Vagrant] boxes are built for [VirtualBox], [Hyper-V], [Azure] and [AWS], and are provisioned using [Chef].

> **Note** All the components, including the core operating systems, share the following characteristics:
>
> * They are based on their publicly available versions. You might need to provide your own license(s) (for example, a valid Windows or Visual Studio license) to start or keep using them after their evaluation periods expire.
> * They are installed using their latest available versions. The latest patches (for example, all the Windows Updates) are applied as well.
> * Unless noted otherwise, they are installed using the default configuration options.

[Overview]: #overview

[Vagrant boxes]: https://app.vagrantup.com/gusztavvargadr/
[Virtual workstations]: https://github.com/gusztavvargadr/workstations/
[BlogWhy]: https://bit.ly/wdywttt5
[BlogHow]: https://bit.ly/wdywttt7

[Packer]: https://www.packer.io/
[Vagrant]: https://www.vagrantup.com/
[VirtualBox]: https://www.virtualbox.org/
[Hyper-V]: https://en.wikipedia.org/wiki/Hyper-V
[Azure]: https://azure.microsoft.com/
[AWS]: https://aws.amazon.com/
[Chef]: https://www.chef.sh/

### Operating systems

The following Vagrant boxes can be used for generic experiments on the respective platforms. They contain the core operating system with the minimum configuration required to make Vagrant work, and some of the commonly used tools installed and options configured for easier provisioning. All the other Vagrant boxes below are based on these configurations as well.

[Operating systems]: #operating-systems

#### Windows

[Windows]: #windows

##### Windows Server

- [Windows Server **latest**][windows-server-latest-box]
    - Windows Server 2019 Standard
    - Windows Server 2016 Standard
- [Windows Server **Standard LTSC**][windows-server-standard-ltsc-box]
    - Windows Server 2019 Standard
    - Windows Server 2016 Standard
- [Windows Server **Standard Core LTSC**][windows-server-standard-core-ltsc-box]
    - Windows Server 2019 Standard Core
    - Windows Server 2016 Standard Core
- [Windows Server **Standard Insider**][windows-server-standard-insider-box]
    - Windows Server 2022 Preview Standard
- [Windows Server **Standard Core Insider**][windows-server-standard-core-insider-box]
    - Windows Server 2022 Preview Standard Core

[windows-server-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-server/
[windows-server-standard-ltsc-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-server-standard/
[windows-server-standard-core-ltsc-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-server-standard-core/
[windows-server-standard-insider-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-server-standard-insider/
[windows-server-standard-core-insider-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-server-standard-core-insider/

##### Windows 10

- [Windows 10 **latest**][windows-10-latest-box]
    - Windows 10 Version 21H1 Enterprise
    - Windows 10 Version 20H2 Enterprise
- [Windows 10 **Enterprise SAC**][windows-10-enterprise-sac-box]
    - Windows 10 Version 21H1 Enterprise
    - Windows 10 Version 20H2 Enterprise
- [Windows 10 **Enterprise LTSC**][windows-10-enterprise-ltsc-box]
    - Windows 10 Version 1809 Enterprise LTSC
- [Windows 10 **Enterprise Insider**][windows-10-enterprise-insider-box]
    - Windows 10 Version 21H1 Insider Preview Enterprise

[windows-10-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-10/
[windows-10-enterprise-sac-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-10-enterprise/
[windows-10-enterprise-ltsc-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-10-enterprise-ltsc/
[windows-10-enterprise-insider-box]: https://app.vagrantup.com/gusztavvargadr/boxes/windows-10-enterprise-insider/

#### Ubuntu

[Ubuntu]: #ubuntu

##### Ubuntu Server

- [Ubuntu Server **latest**][ubuntu-server-latest-box]
    - Ubuntu 16.04 Server LTS
- [Ubuntu Server **LTS**][ubuntu-server-lts-box]
    - Ubuntu 16.04 Server LTS

[ubuntu-server-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/ubuntu-server/
[ubuntu-server-lts-box]: https://app.vagrantup.com/gusztavvargadr/boxes/ubuntu-server-lts/

##### Ubuntu Desktop

- [Ubuntu Desktop **latest**][ubuntu-desktop-latest-box]
    - Ubuntu 16.04 Desktop with XFCE LTS
- [Ubuntu Desktop **XFCE LTS**][ubuntu-desktop-xfce-lts-box]
    - Ubuntu 16.04 Desktop with XFCE LTS

[ubuntu-desktop-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/ubuntu-desktop/
[ubuntu-desktop-xfce-lts-box]: https://app.vagrantup.com/gusztavvargadr/boxes/ubuntu-desktop-xfce-lts/

### Hosting

The following Vagrant boxes can be used for hosting scenarios. They contain the respective hosting tools with the default configuration are based on the core [operating systems].

[Hosting]: #hosting

#### Docker

[Docker]: #docker

##### Docker Windows

- [Docker Windows **latest**][docker-windows-latest-box]
    - Docker 20.10 Enterprise on Windows Server 2019 Standard
- [Docker Windows **Enterprise** on **Windows Server**][docker-windows-enterprise-windows-server-box]
    - Docker 20.10 Enterprise on Windows Server 2019 Standard
- [Docker Windows **Enterprise** on **Windows Server Core**][docker-windows-enterprise-windows-server-core-box]
    - Docker 20.10 Enterprise on Windows Server 2019 Standard Core

[docker-windows-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-windows/
[docker-windows-enterprise-windows-server-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-windows-enterprise-windows-server/
[docker-windows-enterprise-windows-server-core-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-windows-enterprise-windows-server-core/

##### Docker Linux

- [Docker Linux **latest**][docker-linux-latest-box]
    - Docker 20.10 Community on Ubuntu 16.04 Server LTS
- [Docker Linux **Community** on **Ubuntu Server**][docker-linux-community-ubuntu-server-box]
    - Docker 20.10 Community on Ubuntu 16.04 Server LTS
- [Docker Linux **Community** on **Ubuntu Desktop**][docker-linux-community-ubuntu-desktop-box]
    - Docker 20.10 Community on Ubuntu 16.04 Desktop with XFCE LTS
- [Docker Linux **Community** with Docker Desktop on **Windows 10**][docker-linux-community-windows-10-box]
    - Docker 20.10 Community with Docker Desktop on Windows 10 Version 21H1 Enterprise

[docker-linux-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux/
[docker-linux-community-ubuntu-server-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux-community-ubuntu-server/
[docker-linux-community-ubuntu-desktop-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux-community-ubuntu-desktop/
[docker-linux-community-windows-10-box]: https://app.vagrantup.com/gusztavvargadr/boxes/docker-linux-community-windows-10/

#### IIS

- [IIS **latest**][iis-latest-box]
    - IIS 10.0 with .NET on Windows Server 2019 Standard
- [IIS with .NET on **Windows Server**][iis-windows-server-box]
    - IIS 10.0 with .NET on Windows Server 2019 Standard
- [IIS with .NET on **Windows Server Core**][iis-windows-server-core-box]
    - IIS 10.0 with .NET on Windows Server 2019 Standard Core

[IIS]: #iis

[iis-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/iis/
[iis-windows-server-box]: https://app.vagrantup.com/gusztavvargadr/boxes/iis-windows-server/
[iis-windows-server-core-box]: https://app.vagrantup.com/gusztavvargadr/boxes/iis-windows-server-core/

#### SQL Server

- [SQL Server **latest**][sql-server-latest-box]
    - SQL Server 2019 Developer with Management Studio on Windows Server 2019 Standard
    - SQL Server 2017 Developer with Management Studio on Windows Server 2019 Standard
- [SQL Server **Developer** with Management Studio on **Windows Server**][sql-server-developer-windows-server-box]
    - SQL Server 2019 Developer with Management Studio on Windows Server 2019 Standard
    - SQL Server 2017 Developer with Management Studio on Windows Server 2019 Standard

[SQL Server]: #sql-server

[sql-server-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/sql-server/
[sql-server-developer-windows-server-box]: https://app.vagrantup.com/gusztavvargadr/boxes/sql-server-developer-windows-server/

### Development

The following Vagrant boxes can be used for development scenarios including setting up [virtual workstations]. They contain the respective development tools with the common configuration and are based on the core [operating systems].

[Development]: #development

#### Visual Studio

- [Visual Studio **latest**][visual-studio-latest-box]
    - Visual Studio 2019 Community with Docker Desktop on Windows 10 Version 21H1 Enterprise
    - Visual Studio 2017 Community with Docker Desktop on Windows 10 Version 21H1 Enterprise
- [Visual Studio **Community** with Docker Desktop on **Windows 10**][visual-studio-community-windows-10-box]
    - Visual Studio 2019 Community with Docker Desktop on Windows 10 Version 21H1 Enterprise
    - Visual Studio 2017 Community with Docker Desktop on Windows 10 Version 21H1 Enterprise
- [Visual Studio **Professional** with Docker Desktop on **Windows 10**][visual-studio-professional-windows-10-box]
    - Visual Studio 2019 Professional with Docker Desktop on Windows 10 Version 21H1 Enterprise
    - Visual Studio 2017 Professional with Docker Desktop on Windows 10 Version 21H1 Enterprise

[Visual Studio]: #visual-studio

[visual-studio-latest-box]: https://app.vagrantup.com/gusztavvargadr/boxes/visual-studio/
[visual-studio-community-windows-10-box]: https://app.vagrantup.com/gusztavvargadr/boxes/visual-studio-community-windows-10/
[visual-studio-professional-windows-10-box]: https://app.vagrantup.com/gusztavvargadr/boxes/visual-studio-professional-windows-10/

## Getting started

> **Note** The rest of this document covers the details of building virtual machine images and Vagrant boxes, and assumes that you are familiar with the basics of [Packer] and [Vagrant]. If that's not the case, it's recommended that you take a quick look at the [getting][PackerGettingStarted] [started][VagrantGettingStarted] guides.

> **Note** Building the Packer templates have been tested on Windows hosts only, but they are supposed to run on any other platform as well, given that the actual virtualization provider (e.g. VirtualBox) supports it. [Let me know][Contributing] if you encounter any issues and I'm glad to help.

Follow the steps below to install the required tools:

1. Install the [.NET Core SDK][NETCoreSDKInstallation] with [Cake Build][CakeBuildInstallation].
1. Install [Packer][PackerInstallation] and [Vagrant][VagrantInstallation].
1. Install the tools for the virtualization provider you want to use.
    - **VirtualBox** Install [VirtualBox][VirtualBoxInstallation].
    - **Hyper-V** Enable [Hyper-V][HyperVEnabling].
1. Install [Chef Workstation][ChefWorkstationInstallation].

You are now ready to build a virtual machine image and a Vagrant box.

> **Note** It is recommended to set up [caching for Packer][PackerCaching], so you can reuse the downloaded resources (e.g. OS ISOs) across different builds. Make sure you have a bunch of free disk space for the cache and the build artifacts.

[Getting started]: #getting-started

[PackerGettingStarted]: https://www.packer.io/intro/getting-started/install.html
[VagrantGettingStarted]: https://www.vagrantup.com/intro/getting-started/index.html

[NETCoreSDKInstallation]: https://dotnet.microsoft.com/download
[CakeBuildInstallation]: https://www.nuget.org/packages/Cake.Tool/
[PackerInstallation]: https://www.packer.io/docs/install/index.html
[VagrantInstallation]: https://www.vagrantup.com/docs/installation/
[VirtualBoxInstallation]: https://www.virtualbox.org/wiki/Downloads/
[HyperVEnabling]: https://docs.microsoft.com/en-us/virtualization/hyper-v-on-windows/quick-start/enable-hyper-v
[ChefWorkstationInstallation]: https://downloads.chef.io/chef-workstation/

[PackerCaching]: https://www.packer.io/docs/other/environment-variables.html#packer_cache_dir

## Usage

**Contents** [Building base images] | [Building images for distribution] | [Chaining builds further] | [Testing] | [Cleaning up]

This repository uses some [custom wrapper scripts][SourceCoreCake] using [Cake] to generate the Packer templates and the related resources (e.g. the unattended install configuration) required to build the virtual machine images. Besides supporting easier automation, this approach helps with reusing parts of the templates and the
related resources, and makes chaining builds and creating new configurations quite easy.

[Usage]: #usage

[SourceCoreCake]: src/core/cake/
[Cake]: http://cakebuild.net/

### Building base images

Clone this repo [including the submodules][GitCloneRecursive], and navigate to the root directory of the clone in your shell. Type the following command to list all the available templates you can build:

```shell
$ dotnet tool restore
$ dotnet cake [--target=info]
```

The output will be contain the section `info` with the list of the templates:

```
...
========================================
info
========================================
...
ws2019s-virtualbox-core: Info
ws2019s-virtualbox-vagrant: Info
ws2019s-hyperv-core: Info
ws2019s-hyperv-vagrant: Info
...
w102101e-virtualbox-core: Info
w102101e-virtualbox-vagrant: Info
w102101e-hyperv-core: Info
w102101e-hyperv-vagrant: Info
...
ws2019s-iis-virtualbox-core: Info
ws2019s-iis-virtualbox-vagrant: Info
ws2019s-iis-hyperv-core: Info
ws2019s-iis-hyperv-vagrant: Info
...
```

You can filter this further to list only the templates for a given virtual machine image type. For example, to list the templates based on the `Windows Server 2019 Standard` image, invoke the `info` command with the `ws2019s` argument:

```shell
$ dotnet cake [--target=info] --configuration=ws2019s
```

You can use this filtering with all the `dotnet cake` commands below as well. It selects all the templates which contain the specified argument as a substring, so you can filter for components (`ws2019s`, `w102101e`, `iis`, etc.) or providers (`virtualbox`, `hyperv`) easily.

The output will contain only the matching templates:

```
...
========================================
info
========================================
ws2019s-virtualbox-core: Info
ws2019s-virtualbox-vagrant: Info
ws2019s-hyperv-core: Info
ws2019s-hyperv-vagrant: Info
...
```

This means that this configuration supports building native base images (`virtualbox-core`, `hyperv-core`) mainly for reusing them in other configurations, and also, Vagrant boxes for distribution (`virtualbox-vagrant`, `hyperv-vagrant`). Under the hood, the `vagrant` configurations will simply start from the output of the `core` ones, so build times can be reduced significantly.

Now, invoke the `restore` command with the name of the template you want to build to create the resources required by Packer. For example, for VirtualBox, type the following command:

```shell
$ dotnet cake --target=restore --configuration=ws2019s-virtualbox-core
```

This will create the folder `build/ws2019s/virtualbox-core` in the root of your clone with all the files required to invoke the Packer build. This setup is self-contained, so you can adjust the parameters manually in `template.json` or the other resources and / or even copy it to a different machine and simply invoke `packer build template.json` there. Most of the time though, you just simply want to build as it is, as the templates are already preconfigured with some reasonable defaults. This can be done of course with the build script as well:

```shell
$ dotnet cake --target=build --configuration=ws2019s-virtualbox-core
```

This will trigger the Packer build process, which usually requires only patience. Depending on the selected configuration, a few minutes or hours later, the build output will be created, in this case in the `build/ws2019s/virtualbox-core/output` directory in the root of your clone. Virtual machine images like this can be directly used with the respective virtualization provider on the host machine.

[Building base images]: #building-base-images

[GitCloneRecursive]: https://stackoverflow.com/a/4438292

### Building images for distribution

As mentioned above, based on Packer's support for starting builds from some virtualization providers' native image format, builds can reuse the output of a previous build. To build and image which can be distributed (e.g. after applying [Sysprep] as well), type the following command:

```shell
$ dotnet cake --target=build --configuration=ws2019s-virtualbox-vagrant
```

Note that this will include restoring the build folder with the template and the related resources automatically, and then invoking the build process in a single step. It will also reuse the output of the `ws2019s-virtualbox-core` build, so it does not need to do the same steps for a Vagrant box the original build already included (e.g. the core OS installation itself, installing Windows updates, etc.). Once the build completes, the Vagrant box will be available in the `build/ws2019s/virtualbox-vagrant/output` folder.

The same approach works for Hyper-V as well:

```shell
$ dotnet cake --target=build --configuration=ws2019s-hyperv-core
$ dotnet cake --target=build --configuration=ws2019s-hyperv-vagrant
```

As you can expect, for these samples the build artifacts will be created in the `builds/ws2019s` folder as well, this time under the `hyperv-vagrant/output` subfolder. You can use the standard options to [distribute them][VagrantDistribute] to be consumed in Vagrant.

[Building images for distribution]: #building-images-for-distribution

[Sysprep]: https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/sysprep--generalize--a-windows-installation
[VagrantDistribute]: https://www.vagrantup.com/docs/boxes/base.html#distributing-the-box

### Chaining builds further

Similarly to the process above, you can use build chaining to build more complex boxes. For example, the configuration for `Windows Server 2019 Standard` with `IIS` can be built like this:

```shell
$ dotnet cake --target=build --configuration=ws2019s-virtualbox-core
$ dotnet cake --target=build --configuration=ws2019s-iis-virtualbox-core
$ dotnet cake --target=build --configuration=ws2019s-iis-virtualbox-vagrant
```

As in the previous `ws2019s` sample, for this configuration the `ws2019s-iis-virtualbox-core` build will start from the output of `ws2019s-virtualbox-core` instead of starting with the core OS installation. Chanining builds like this has no limitations, so you can use this approach to build images with any number of components very effectively.

Note that the script can invoke the build of the dependencies automatically, so for the previous example you can simply type:

```shell
$ dotnet cake --target=build --configuration=ws2019s-iis-virtualbox-vagrant
```

This will in turn invoke the `restore` and `build` stages for the `ws2019s-virtualbox-core` and `ws2019s-iis-virtualbox-core` images as well. By default, `restore` and `build` is skipped if the output from a previous build exists. You can force the build to run again using the `rebuild` command instead, which will `clean` the build directories first.

Again, this works for Hyper-V as well:

```shell
$ dotnet cake --target=build --configuration=ws2019s-iis-hyperv-vagrant
```

Similarly, this will in turn build the `ws2019s-hyperv-core` and `ws2019s-iis-hyperv-core` images first if they are missing.

[Chaining builds further]: #chaining-builds-further

### Testing

To help testing the build results, the reposiory contains a simple [Vagrantfile] to create virtual machines using directly the build outputs. You can play around with the [Vagrant CLI][VagrantCLI] yourself, or let the build script manage it for you.

For example, to test the `ws2019s` configuration, from the root of your clone you can type the following command to use the box files in the `build\ws2019s` folder:

```shell
$ dotnet cake --target=test --configuration=ws2019s-virtualbox-vagrant
```

This will import the locally built Vagrant box temporarily with the name `ws2019s-build` and will use that to spin up a new virtual machine. It also outputs some basic diagnostics information to help quickly checking the installations.

[Testing]: #testing

[Vagrantfile]: Vagrantfile
[VagrantCLI]: https://www.vagrantup.com/docs/cli/

### Cleaning up

Though the `build` folders are excluded by default from the repository, they can consume significant disk space. You can manually delete the folders, but the build script provides support for this as well:

```shell
$ dotnet cake --target=clean --configuration=ws2019s-iis-virtualbox-vagrant
```

Using the filtering, to clean up the artifacts of all the VirtualBox builds, you can type:

```shell
$ dotnet cake --target=clean --configuration=virtualbox
```

Omitting this parameter will apply the command to all the templates, so the following command will clean up everything:

```shell
$ dotnet cake --target=clean
```

> **Note** The `clean` command cleans up dependencies recursively, including the eventually imported Vagrant boxes and virtual machines created using the `test` command.

[Cleaning up]: #cleaning-up

## Next steps

Take a look at the repository of [virtual workstations] to easily automate and share your development environment configurations using the Vagrant boxes above.

[Next steps]: #next-steps

## Contributing

Feedback, [issues] or [pull requests] are welcome and are greatly appreciated. Check out the [milestones] for the list of planned releases.

[Contributing]: #contributing

[Issues]: https://github.com/gusztavvargadr/packer/issues/
[Pull requests]: https://github.com/gusztavvargadr/packer/pulls/
[Milestones]: https://github.com/gusztavvargadr/packer/milestones/

## Changes

 Some changes have been made to the original repo:
  - Remove any Chef dependencies (plan to use Ansible for any configuration management)
  - Addition of French Windows install

### Steps
- Install [ADK](https://docs.microsoft.com/en-us/windows-hardware/get-started/adk-install) (necessary to build images on a Windows box)
- Add `C:\Program Files (x86)\Windows Kits\10\Assessment and Deployment Kit\Deployment Tools\x86\Oscdimg` to PATH environment variable
- Install windows-update provisioner plugin (replaces Chef provisioning)
 ```powershell
 $zipFile="packer-provisioner-windows-update_0.11.0_windows_amd64.zip"
 Invoke-WebRequest https://github.com/rgl/packer-plugin-windows-update/releases/download/v0.11.0/$zipFile -OutFile ~/Downloads/$zipFile
 Expand-Archive -Path ~/Downloads/$zipFile -DestinationPath $env:APPDATA\packer.d\plugins\ -Force
 ```
- Set the Packer Cache Dir (to avoid downloading the same iso multiple times ): `$env:PACKER_CACHE_DIR="C:/packer/"`

To create Vagrant box for Hyper-V :
```powershell

dotnet cake --target=rebuild --configuration=ws2019sfrca-hyperv-vagrant --verbosity=verbose
```

To simply add Vagrant box locally :
```shell
vagrant box add  windows-server-standard-fr  .\build\ws2019sfrca\hyperv-vagrant\output\package\vagrant.box --force
```
To publish box to Vagrant Cloud :
```
dotnet cake --target=publish --configuration=ws2019sfrca-hyperv-vagrant --verbosity=verbose
```


### Issues

This repo hasn't been converted to the new packer HCL2 syntax. Newer version of plugins (e.g. windows-update) and don't seem to be supported without this conversion.

## Resources

This repository could not exist without the following great technologies:

- [Packer]
- [Vagrant]
- [VirtualBox]
- [Hyper-V]
- [Azure]
- [AWS]
- [Chef]

This repository borrows awesome ideas and solutions from the following sources:

- [Gusztáv Varga]
- [Matt Wrock]
- [Jacqueline]
- [Joe Fitzgerald]
- [Boxcutter]
- [Bento]

[Resources]: #resources
[Gusztáv Varga]: https://github.com/gusztavvargadr/packer
[Matt Wrock]: https://github.com/mwrock/packer-templates/
[Jacqueline]: https://github.com/jacqinthebox/packer-templates/
[Joe Fitzgerald]: https://github.com/joefitzgerald/packer-windows/
[Boxcutter]: https://github.com/boxcutter/windows/
[Bento]: https://github.com/chef/bento/
