---
description: Este artigo fornece um índice de documentação sobre as APIs do Win32 disponíveis para recursos e tecnologias do Windows.
ms.assetid: FF115416-220F-4FCD-8690-F9C0890CD6CC
title: Tecnologias de aplicativos de desktop
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5b6e077c5f8fde2e723fbf9a971cbe09b8d008
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/19/2021
ms.locfileid: "105765284"
---
# <a name="desktop-app-technologies"></a>Tecnologias de aplicativos de desktop

Esta seção fornece orientações detalhadas e exemplos de código sobre os recursos do Windows que estão disponíveis para aplicativos da área de trabalho usando a API do Win32.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição  |  
|----------------------------------|---|
| [Acessibilidade](accessibility/accessibility.md) | Fornece orientação para desenvolvedores do Windows que projetam aplicativos acessíveis, desenvolvedores de tecnologia assistencial que criam ferramentas como leitores de tela e lentes de desenvolvimento, além de engenheiros de teste de software criando scripts automatizados para testar aplicativos do Windows. |
| [Interface do usuário da Área de Trabalho](windows-application-ui-development.md) | Fornece informações que permitem que você desenvolva interfaces gráficas do usuário para seus aplicativos, incluindo recursos como Windows e mensagens, recursos e controles. |
| [Ambiente de desktop](user-interface.md) | Fornece orientação para integrar e estender os recursos voltados para o usuário da área de trabalho do Windows, incluindo a barra de tarefas, a área de trabalho e o explorador de arquivos. |
| [Instalação e manutenção de aplicativos](application-installing-and-servicing.md) | Fornece informações sobre como usar APIs e serviços fornecidos pelo Windows para instalar, gerenciar e atender seus aplicativos de desktop. |
| [Áudio e vídeo](audio-and-video.md) | Fornece orientação sobre como usar os recursos de áudio e vídeo fornecidos pelo Windows. |
| [Acesso a dados e armazenamento](data-access-and-storage.md) | Fornece informações sobre o acesso a dados e recursos de armazenamento que você pode usar em seus aplicativos de área de trabalho, incluindo o gerenciamento do sistema de arquivos e mecanismos de sincronização de nuvem.  |
| [Dispositivos](devices.md) | Descreve as APIs para interagir com dispositivos e sensores. |
| [Diagnóstico](diagnostics.md) | Fornece orientação sobre depuração e tratamento de erros, criação de perfil de desempenho, monitoramento de rede e outros recursos de diagnóstico. |
| [Documentos e impressão](printdocs/documents-and-printing.md) | Descreve os documentos e os recursos de impressão do Windows que permitem que os aplicativos salvem, exibam e imprimam.  |
| [Elementos gráficos e jogos](graphics-and-multimedia.md) | Fornece informações sobre os recursos de gráficos e jogos do Windows, incluindo DirectX e imagens digitais.  |
| [Rede e Internet](networking.md) | Fornece orientação sobre a rede e os recursos relacionados à Internet do Windows, incluindo gerenciamento de rede, APIs HTTP e RPC (chamada de procedimento remoto). |
| [Segurança e identidade](security.md) | Fornece informações sobre autenticação, autorização, criptografia e outros recursos de segurança do Windows. |
| [Serviços do sistema](system-services.md) | Fornece orientação sobre OS recursos fundamentais do sistema operacional, como processos e threads, serviços, bibliotecas de vínculo dinâmico, COM, o registro e muito mais. |

<!--
<br/>

| User Interface and accessibility | System services and fundamentals  |  Audio, video, and graphics  |
|----------------------------------|---|----|
| [Desktop User Interface](windows-application-ui-development.md)<br/>[Windows and messages](winmsg/windowing.md)<br/>[Desktop Window Manager](dwm/dwm-overview.md)<br/>[Menus and other resources](menurc/resources.md)<br/>[Dialog boxes](dlgbox/dialog-boxes.md)<br/>[Data exchange](dataxchg/data-exchange.md)<br/>[High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)<br/>[Windows controls (Win32)](controls/window-controls.md)<br/>[Desktop environment and shell](user-interface.md)<br/>[Windows Property System](properties/windows-properties-system.md)<br/>[Accessibility](accessibility.md) | [System services](system-services.md)<br/>[Component Object Model (COM)](com/component-object-model--com--portal.md)<br/>[COM+](cossdk/component-services-portal.md)<br/>[Structured storage](stg/structured-storage-start-page.md)<br/>[Dynamic-link libraries](dlls/dynamic-link-libraries.md)<br/>[Interprocess communications](ipc/interprocess-communications.md)<br/>[Memory management](memory/memory-management.md)<br/>[Power management](power/power-management-portal.md)<br/>[Processes and threads](procthread/processes-and-threads.md)<br/>[Services](services/services.md)<br/>[Synchronization](sync/synchronization.md)<br/>[Windows system information](sysinfo/windows-system-information.md) | [Audio and video technologies](audio-and-video.md)<br/>[Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)<br/>[DirectShow](directshow/directshow.md)<br/>[Windows Multimedia](multimedia/windows-multimedia-start-page.md)<br/>[Graphics and gaming technologies](graphics-and-multimedia.md)<br/>[DirectX](directx.md)<br/>[Direct2D](direct2d/direct2d-portal.md)<br/>[Direct3D](direct3d.md)<br/>[Windows GDI](gdi/windows-gdi.md)<br/>[GDI+](gdiplus/-gdiplus-gdi-start.md)<br/>[OpenGL](opengl/opengl.md)<br/>[Windows Imaging Component](wic/-wic-lh.md) |

<br/>

| Networking and Internet | Data access and storage  |  Devices, documents, and printing  |
|----------------------------------|---|----|
| [Networking and Internet overview](networking.md)<br/>[Remote Procedure Call](rpc/rpc-start-page.md)<br/>[Delivery optimization](delivery_optimization/delivery-optimization-portal.md)<br/>[Network interfaces](network-interfaces.md)<br/>[Network management](netmgmt/network-management.md)<br/>[Network share management](netshare/network-share-management.md)<br/>[Windows networking](wnet/windows-networking-wnet-.md)<br/>[Windows Sockets 2](winsock/windows-sockets-start-page-2.md)<br/>[Wireless networking](wireless-networking.md) | [Data access and storage overview](data-access-and-storage.md)<br/>[Local file systems](fileio/file-systems.md)<br/>[Distributed File System](dfs/distributed-file-system.md)<br/>[Projected File System](projfs/projected-file-system.md)<br/>[Cloud sync engines](cfapi/cloud-files-api-portal.md)<br/>[Virtual Storage](VStor/virtual-storage.md)<br/>[Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)<br/>[Backup](backup.md) | [Devices overview](devices.md)<br/>[Communications resources](devio/communications-resources.md)<br/>[Location API](locationapi/windows-location-api-portal.md)<br/>[Sensor API](sensorsapi/portal.md)<br/>[UPnP APIs](upnp/universal-plug-and-play-start-page.md)<br/>[Windows Portable Devices](windows-portable-devices.md)<br/>[Documents and printing](printdocs/documents-and-printing.md) |

<br/>

| Security and identity | Diagnostics and testing  |  Packaging and installation  |
|----------------------------------|---|----|
| [Security and identity overview](security.md)<br/>[Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)<br/>[Authentication](secauthn/authentication-portal.md)<br/>[Authorization](secauthz/authorization-portal.md)<br/>[Certificate Enrollment API](seccertenroll/certenroll-portal.md)<br/>[Cryptography (CNG)](seccng/cng-portal.md)<br/>[Rights Management](SrvNodes/rights-management.md)<br/>[Security Management](secmgmt/management-portal.md)<br/>[TPM Base Services](tbs/tpm-base-services-portal.md)<br/>[Windows Biometric Framework](secbiomet/biometric-service-api-portal.md) | [Diagnostics overview](diagnostics.md)<br/>[Debugging and error handling](debugging-and-error-handling.md)<br/>[Network Monitor](netmon2/network-monitor.md)<br/>[System Monitor](sysmon/system-monitor-portal.md)<br/>[Performance counters](perfctrs/performance-counters-portal.md)<br/>[Windows error reporting](wer/windows-error-reporting.md)<br/>[Windows events](events/windows-events.md)<br/>[TraceLogging](tracelogging/trace-logging-portal.md)<br/>[Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index) | [MSIX packaging](//docs.microsoft.com/windows/msix)<br/>[Application install and servicing](application-installing-and-servicing.md)<br/>[Side-by-side assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)<br/>[Packaging and query of UWP apps](appxpkg/appx-portal.md)<br/>[Windows Installer](msi/windows-installer-portal.md)<br/>[Desktop Application Program](appxpkg/windows-desktop-application-program.md)<br/>[Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/) |

-->

<!--
:::row:::
    :::column:::
        ![User Interface and accessibility](/media/illustrations/bcs-partner-advanced-management-add-user-1.svg?branch=master)
        ### User Interface and accessibility
        * [Desktop User Interface](windows-application-ui-development.md)
        * [Windows and messages](winmsg/windowing.md)
        * [Desktop Window Manager](dwm/dwm-overview.md)
        * [Dialog boxes](dlgbox/dialog-boxes.md)
        * [Menus and other resources](menurc/resources.md)
        * [Data exchange](dataxchg/data-exchange.md)
        * [High DPI](hidpi/high-dpi-desktop-application-development-on-windows.md)
        * [Windows controls (Win32)](controls/window-controls.md)
        * [Desktop environment and shell](user-interface.md)
        * [Windows Property System](properties/windows-properties-system.md)
        * [Accessibility](accessibility.md)
    :::column-end:::
    :::column:::
        ![System and fundamentals](/media/illustrations/biztalk-get-started-get-started.svg?branch=master)
        ### System services and fundamentals
        * [System services](system-services.md)
        * [Component Object Model (COM)](com/component-object-model--com--portal.md)
        * [COM+](cossdk/component-services-portal.md)
        * [Structured storage](stg/structured-storage-start-page.md)
        * [Dynamic-link libraries](dlls/dynamic-link-libraries.md)
        * [Interprocess communications](ipc/interprocess-communications.md)
        * [Memory management](memory/memory-management.md)
        * [Power management](power/power-management-portal.md)
        * [Processes and threads](procthread/processes-and-threads.md)
        * [Services](services/services.md)
        * [Synchronization](sync/synchronization.md)
        * [Windows system information](sysinfo/windows-system-information.md)
    :::column-end:::
    :::column:::
        ![Audio, video, and graphics](/media/illustrations/virtualization-containers-samples.svg?branch=master)
        ### Audio, video, and graphics
        * [Audio and video technologies](audio-and-video.md)
        * [Core Audio APIs](coreaudio/core-audio-apis-in-windows-vista.md)
        * [DirectShow](directshow/directshow.md)
        * [Windows Multimedia](multimedia/windows-multimedia-start-page.md)
        * [Graphics and gaming technologies](graphics-and-multimedia.md)
        * [DirectX](directx.md)
        * [Direct2D](direct2d/direct2d-portal.md)
        * [Direct3D](direct3d.md)
        * [Windows GDI](gdi/windows-gdi.md)
        * [GDI+](gdiplus/-gdiplus-gdi-start.md)
        * [OpenGL](opengl/opengl.md)
        * [Windows Imaging Component](wic/-wic-lh.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Networking and Internet](/media/illustrations/teams-voice-deployment.svg?branch=master)
        ### Networking and Internet
        * [Networking and Internet overview](networking.md)
        * [Remote Procedure Call](rpc/rpc-start-page.md)
        * [Delivery Optimization](delivery_optimization/delivery-optimization-portal.md)
        * [Network interfaces](network-interfaces.md)
        * [Network Management](netmgmt/network-management.md)
        * [Network Share Management](netshare/network-share-management.md)
        * [Windows Networking](wnet/windows-networking-wnet-.md)
        * [Windows Sockets 2](winsock/windows-sockets-start-page-2.md)
        * [Wireless Networking](wireless-networking.md)
    :::column-end:::
    :::column:::
        ![Data access and storage](/media/illustrations/azure-architecture-patterns.svg?branch=master)
        ### Data access and storage
        * [Data access and storage overview](data-access-and-storage.md)
        * [Local File Systems](fileio/file-systems.md)
        * [Distributed File System](dfs/distributed-file-system.md)
        * [Projected File System](projfs/projected-file-system.md)
        * [Cloud Sync Engines](cfapi/cloud-files-api-portal.md)
        * [Virtual Storage](VStor/virtual-storage.md)
        * [Background Intelligent Transfer Service](bits/background-intelligent-transfer-service-portal.md)
        * [Backup](backup.md)
    :::column-end:::
    :::column:::
        ![Devices, documents, and printing](/media/illustrations/virtualization-hperv-server-doc-archive.svg?branch=master)
        ### Devices, documents, and printing
        * [Devices overview](devices.md)
        * [Communications Resources](devio/communications-resources.md)
        * [Location API](locationapi/windows-location-api-portal.md)
        * [Sensor API](sensorsapi/portal.md)
        * [UPnP APIs](upnp/universal-plug-and-play-start-page.md)
        * [Windows Portable Devices](windows-portable-devices.md)
        * [Documents and Printing](printdocs/documents-and-printing.md)
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Security and identity](/media/illustrations/bcs-partner-advanced-management-password-3.svg?branch=master)
        ### Security and identity
        * [Security and identity overview](security.md)
        * [Antimalware Scan Interface](amsi/antimalware-scan-interface-portal.md)
        * [Authentication](secauthn/authentication-portal.md)
        * [Authorization](secauthz/authorization-portal.md)
        * [Certificate Enrollment API](seccertenroll/certenroll-portal.md)
        * [Cryptography (CNG)](seccng/cng-portal.md)
        * [Rights Management](SrvNodes/rights-management.md)
        * [Security Management](secmgmt/management-portal.md)
        * [TPM Base Services](tbs/tpm-base-services-portal.md)
        * [Windows Biometric Framework](secbiomet/biometric-service-api-portal.md)
    :::column-end:::
    :::column:::
        ![Diagnostics and testing](/media/illustrations/team-services-dev-ops-test.svg?branch=master)
        ### Diagnostics and testing
        * [Diagnostics overview](diagnostics.md)
        * [Debugging and error handling](debugging-and-error-handling.md)
        * [Network Monitor](netmon2/network-monitor.md)
        * [System Monitor](sysmon/system-monitor-portal.md)
        * [Performance counters](perfctrs/performance-counters-portal.md)
        * [Windows error reporting](wer/windows-error-reporting.md)
        * [Windows events](events/windows-events.md)
        * [TraceLogging](tracelogging/trace-logging-portal.md)
        * [Debugging tools for Windows](//docs.microsoft.com/windows-hardware/drivers/debugger/index)
    :::column-end:::
    :::column:::
        ![Packaging and installation](/media/illustrations/biztalk-host-integration-install-configure.svg?branch=master)
        ### Packaging and installation
        * [MSIX packaging and deployment](//docs.microsoft.com/windows/msix)
        * [Application Installation and Servicing](application-installing-and-servicing.md)
        * [Isolated Applications and Side-by-side Assemblies](sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)
        * [Packaging, deployment, and query of UWP apps](appxpkg/appx-portal.md)
        * [Windows Installer](msi/windows-installer-portal.md)
        * [Windows Desktop Application Program](appxpkg/windows-desktop-application-program.md)
        * [Windows containers](//docs.microsoft.com/virtualization/windowscontainers/about/)
    :::column-end:::
:::row-end:::
-->
