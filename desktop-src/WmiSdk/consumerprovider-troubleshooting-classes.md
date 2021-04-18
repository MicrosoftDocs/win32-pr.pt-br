---
description: A tabela a seguir lista a solução de problemas de classes de evento que são geradas pelas operações do provedor de consumidor de eventos.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classes de solução de problemas do consumidorprovider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 536c23fb35ca6a4d2146cf87782768c51f37a6ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105813759"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classes de solução de problemas do consumidorprovider

A tabela a seguir lista a solução de problemas de classes de evento que são geradas pelas operações do [*provedor de consumidor de eventos*](gloss-e.md) .

Você pode assinar as notificações do [**MSFT \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) da classe base abstrata para obter todos os eventos a seguir.



|                                                                                                 |                                                                                 |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_WMIPROVIDEREVENT MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Classe pai para todos os eventos do provedor de consumidor.                                  |
| [**\_WMICONSUMERPROVIDERLOADED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Define a ativação bem-sucedida do objeto COM do provedor de consumidor de evento.    |
| [**\_WMICONSUMERPROVIDERUNLOADED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Define a desativação bem-sucedida do objeto COM do provedor de consumidor de evento.  |
| [**\_WMICONSUMERPROVIDERSINKLOADED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Define a ativação bem-sucedida do objeto de coletor do provedor de consumidor de evento.   |
| [**\_WMICONSUMERPROVIDERSINKUNLOADED MSFT**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Define a desativação bem-sucedida do objeto de coletor do provedor de consumidor de eventos. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas do WMI](wmi-troubleshooting.md)
</dt> <dt>

Solução de problemas do WMI
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
