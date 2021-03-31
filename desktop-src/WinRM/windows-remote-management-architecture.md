---
title: Arquitetura de Gerenciamento Remoto do Windows
description: A arquitetura de Gerenciamento Remoto do Windows consiste em componentes nos computadores cliente e servidor.
ms.assetid: 82e67851-fe46-4bb0-8278-9718b5e0c7ae
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0f5576913c5e4a1f2a105fb77e2282dc682c6659
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641571"
---
# <a name="windows-remote-management-architecture"></a>Arquitetura de Gerenciamento Remoto do Windows

A arquitetura de Gerenciamento Remoto do Windows consiste em componentes nos computadores cliente e servidor. A ilustração a seguir mostra os componentes em ambos os computadores, como os componentes interagem com outros componentes e o protocolo que é usado para se comunicar entre os computadores.

![arquitetura do WinRM](images/winrm-architecture.png)

## <a name="requesting-client"></a>Solicitando cliente

Os seguintes componentes do WinRM residem no computador que está executando o script que solicita dados.

-   Aplicativo WinRM

    Essa é a ferramenta de linha de comando do script ou do **WinRM** que usa a API de script do WinRM para fazer chamadas para dados de solicitação ou para executar métodos. Para obter mais informações, consulte a [API de script do WinRM](winrm-scripting-api.md).

-   WSMAuto.dll

    A camada de automação que fornece suporte a scripts.

-   WsmCL.dll

    Camada C API no sistema operacional.

-   API HTTP

    O WinRM requer suporte para transporte HTTP e HTTPS.

## <a name="responding-server"></a>Respondendo ao servidor

Os seguintes componentes do WinRM residem no computador que está respondendo.

-   API HTTP

    O WinRM requer suporte para transporte HTTP e HTTPS.

-   WSMAuto.dll

    A camada de automação que fornece suporte a scripts.

-   WsmCL.dll

    Camada C API no sistema operacional.

-   WsmSvc.dll

    Serviço de [*escuta*](windows-remote-management-glossary.md) do WinRM.

-   WsmProv.dll

    Subsistema do provedor.

-   WsmRes.dll

    Arquivo de recurso.

-   WsmWmiPl.dll

    [*Plug-in WMI*](windows-remote-management-glossary.md). Isso permite que você obtenha dados WMI por meio do WinRM.

-   Driver de IPMI (interface de gerenciamento de plataforma inteligente) e provedor IPMI WMI

    Esses componentes fornecem dados de hardware que são solicitados usando as classes IPMI. Para obter mais informações, consulte [provedor IPMI](/previous-versions/windows/desktop/ipmiprv/ipmi-provider). O hardware do BMC deve ter sido detectado pelo SMBIOS ou pelo dispositivo criado manualmente pelo carregamento do driver. Para obter mais informações, consulte [instalação e configuração para gerenciamento remoto do Windows](installation-and-configuration-for-windows-remote-management.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre Gerenciamento Remoto do Windows](about-windows-remote-management.md)
</dt> </dl>

 

 