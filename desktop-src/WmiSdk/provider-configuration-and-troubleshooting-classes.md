---
description: A classe de provedores de MSFT \_ e as classes de solução de problemas de WMI são um grupo de classes de evento MSFT que são associadas a eventos de provedor WMI.
ms.assetid: 5eaf7026-87bf-416b-9a6d-7f92f85b0882
ms.tgt_platform: multiple
title: Configuração do provedor e classes de solução de problemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be63fb5693898541bffae2abcb05b7595ae7fc9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105793694"
---
# <a name="provider-configuration-and-troubleshooting-classes"></a>Configuração do provedor e classes de solução de problemas

A classe de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) e as classes de solução de problemas de WMI são um grupo de [classes de evento MSFT](msft-classes.md) que são associadas a eventos de provedor WMI.

A classe de [**\_ provedores de MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-providers) contém informações de configuração para provedores e inclui os seguintes métodos que permitem carregar e descarregar provedores, ou suspender e retomar operações do provedor:

-   [**Método Load da classe de \_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers)
-   [**Método UnLoad da classe de \_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/unload-method-in-class-msft-providers)
-   [**Método resume da classe de \_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/resume-method-in-class-msft-providers)
-   [**Método Suspend da classe de \_ provedores MSFT**](/previous-versions/windows/desktop/wmisystemprov/suspend-method-in-class-msft-providers)

As [classes de solução de problemas do WMI](wmi-troubleshooting-classes.md) são nomeadas para indicar se o evento é acionado antes ou depois de um evento de provedor. Por exemplo, o objeto [**MSFT \_ WmiProvider \_ AccessCheck \_ pre**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-pre) é gerado imediatamente antes de chamar a implementação do provedor de **IWbemEventSecurity:: AccessCheck**, enquanto o objeto de [**\_ \_ \_ postagem WmiProvider AccessCheck do MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-accesscheck-post) é chamado imediatamente após.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Classes de solução de problemas do WMI](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
