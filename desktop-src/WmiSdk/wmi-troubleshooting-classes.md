---
description: O WMI fornece um conjunto de classes de solução de problemas que os scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações básicas do WMI e do provedor.
ms.assetid: 631e0cce-0e83-42e5-a381-e96b1f70d6f9
ms.tgt_platform: multiple
title: Classes de solução de problemas do WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65b3972ba59c80a1495916ab24a72f6e93bef8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922776"
---
# <a name="wmi-troubleshooting-classes"></a>Classes de solução de problemas do WMI

O WMI fornece um conjunto de classes de solução de problemas que os scripts e aplicativos podem usar para obter informações sobre o estado interno do WMI durante as operações básicas do WMI e do provedor. Para obter mais informações sobre solução de problemas do WMI, consulte solução de problemas do [WMI](wmi-troubleshooting.md) e [configuração do provedor e classes de solução de problemas](provider-configuration-and-troubleshooting-classes.md).

O WMI tem várias classes básicas de solução de problemas para operações de provedor e núcleo do WMI:

-   [**\_Contadores de WmiProvider do MSFT \_**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-counters)

    Apenas uma dessas classes é encontrada em cada sistema de computador. Ele fornece contagens de vários tipos de operações de provedor nesse sistema.

-   [**\_WMISELFEVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent)

    As classes de solução de problemas de evento derivam de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent). As consultas dessa classe retornam instâncias de classes de evento, como [**MSFT \_ WmiThreadPoolCreated**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated) ou [**MSFT \_ WmiProvider \_ CreateInstanceEnumAsyncEvent \_ post**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiprovider-createinstanceenumasyncevent-post).

    A lista a seguir fornece links para diferentes categorias de classes de evento derivadas de [**MSFT \_ WmiSelfEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiselfevent):

    -   [Classes de solução de problemas de eventos do provedor](provider-event-troubleshooting-classes.md)
    -   [Classes de solução de problemas do consumidorprovider](consumerprovider-troubleshooting-classes.md)
    -   [Classes de solução de problemas de eventos do serviço WMI](wmi-service-event-troubleshooting-classes.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
