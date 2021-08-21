---
description: O WMI fornece um conjunto de classes de solução de problemas que scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações do provedor e do núcleo do WMI.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classes de solução de problemas do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d3c5f1d40cd5da9e61ff289fc0b137ec7613ec8156fb0acc4f225e793a8407
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049854"
---
# <a name="wmi-troubleshooting-classes"></a>Classes de solução de problemas do WMI

O WMI fornece um conjunto de classes de solução de problemas que scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações do provedor e do núcleo do WMI. Para obter mais informações sobre a solução de problemas do WMI, consulte [WMI Troubleshooting](wmi-troubleshooting.md) and [Provider Configuration and Troubleshooting Classes](provider-configuration-and-troubleshooting-classes.md).

O WMI tem várias classes básicas de solução de problemas para operações de provedor e núcleo WMI:

-   [**Contadores \_ WmiProvider do MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Somente uma dessas classes é encontrada em cada sistema de computador. Ele fornece contagens de vários tipos de operações de provedor nesse sistema.

-   [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    As classes de solução de problemas de evento [**derivam de MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). Consultas dessa classe retornam instâncias de classes de evento como [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) ou [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ Post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    A lista a seguir fornece links para diferentes categorias de classes de evento derivadas de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Classes de solução de problemas de eventos do provedor](provider-event-troubleshooting-classes.md)
    -   [Classes de solução de problemas ConsumerProvider](consumerprovider-troubleshooting-classes.md)
    -   [Classes de solução de problemas de eventos do serviço WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
