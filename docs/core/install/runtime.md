---
title: Install .NET Core runtime on Windows, Linux, and macOS - .NET Core
description: Learn how to install .NET Core on Windows, Linux, and macOS. Discover the dependencies required to run .NET Core apps.
author: thraka
ms.author: adegeo
ms.date: 12/04/2019
ms.custom: "updateeachrelease"
zone_pivot_groups: operating-systems-set-one
---

# Install the .NET Core Runtime

In this article, you'll learn how to download and install the .NET Core runtime. The .NET Core runtime is used to run apps created with .NET Core.

::: zone pivot="os-windows"

## Install with an installer

Windows has standalone installers that can be used to install the .NET Core 3.1 runtime:

- [x64 (64-bit) CPUs](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [x86 (32-bit) CPUs](https://dotnet.microsoft.com/download/dotnet-core/3.1)

::: zone-end

::: zone pivot="os-macos"

## Install with an installer

macOS has standalone installers that can be used to install the .NET Core 3.1 runtime:

- [x64 (64-bit) CPUs](https://dotnet.microsoft.com/download/dotnet-core/3.1)

::: zone-end

::: zone pivot="os-linux"

## Install with a package manager

You can install the .NET Core Runtime with many of the common Linux package managers. For more information, see [Linux Package Manager - Install .NET Core](linux-package-manager-rhel7.md).

::: zone-end

::: zone pivot="os-windows"

## Install with PowerShell automation

The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for automation and non-admin installs of the runtime. You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).

The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET Core 3.1. You can choose a specific release by specifying the `Channel` switch. Include the `Runtime` switch to install a runtime. Otherwise, the script installs the [SDK](sdk.md).

```powershell
dotnet-install.ps1 -Channel 3.1 -Runtime aspnetcore
```

> [!NOTE]
> The command above installs the ASP.NET Core runtime for maximum compatability. The ASP.NET Core runtime also includes the standard .NET Core runtime.

::: zone-end

::: zone pivot="os-linux,os-macos"

## Install with bash automation

The [dotnet-install scripts](../tools/dotnet-install-script.md) are used for automation and non-admin installs of the runtime. You can download the script from the [dotnet-install script reference page](../tools/dotnet-install-script.md).

The script defaults to installing the latest [long term support (LTS)](https://dotnet.microsoft.com/platform/support/policy/dotnet-core) version, which is .NET Core 3.1. You can choose a specific release by specifying the `current` switch. Include the `runtime` switch to install a runtime. Otherwise, the script installs the [SDK](sdk.md).

```bash
./dotnet-install.sh --current 3.1 --runtime aspnetcore
```

> [!NOTE]
> The command above installs the ASP.NET Core runtime for maximum compatability. The ASP.NET Core runtime also includes the standard .NET Core runtime.

::: zone-end

## All .NET Core downloads

You can download and install .NET Core directly with one of the following links:

- [.NET Core 3.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/3.1)
- [.NET Core 3.0 downloads](https://dotnet.microsoft.com/download/dotnet-core/3.0)
- [.NET Core 2.2 downloads](https://dotnet.microsoft.com/download/dotnet-core/2.2)
- [.NET Core 2.1 downloads](https://dotnet.microsoft.com/download/dotnet-core/2.1)

## Docker

Containers provide a lightweight way to isolate your application from the rest of the host system. Containers on the same machine share just the kernel and use resources given to your application.

.NET Core can run in a Docker container. Official .NET Core Docker images are published to the Microsoft Container Registry (MCR) and are discoverable at the [Microsoft .NET Core Docker Hub repository](https://hub.docker.com/_/microsoft-dotnet-core/). Each repository contains images for different combinations of the .NET (SDK or Runtime) and OS that you can use.

Microsoft provides images that are tailored for specific scenarios. For example, the [ASP.NET Core repository](https://hub.docker.com/_/microsoft-dotnet-core-aspnet/) provides images that are built for running ASP.NET Core apps in production.

For more information about using .NET Core in a Docker container, see [Introduction to .NET and Docker](../docker/introduction.md) and [Samples](https://github.com/dotnet/dotnet-docker/blob/master/samples/README.md).

## Next steps

- [How to check if .NET Core is already installed](how-to-detect-installed-versions.md).
