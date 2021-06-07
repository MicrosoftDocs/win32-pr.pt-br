---
description: A tabela a seguir lista a solução de problemas de classes de evento geradas por operações do provedor de consumidor de eventos.
ms.assetid: dd685a41-8eae-4977-ab94-902dd8dddcc9
ms.tgt_platform: multiple
title: Classes de solução de problemas ConsumerProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 740b8c0eb1884181fa84efe26e0611dda4b1712f
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443607"
---
# <a name="consumerprovider-troubleshooting-classes"></a>Classes de solução de problemas ConsumerProvider

A tabela a seguir lista a solução de problemas de classes de evento geradas por operações [*do provedor de consumidor de*](gloss-e.md) eventos.

Você pode assinar as notificações da classe base [**abstrata MSFT \_ ProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) para obter todos os eventos a seguir.



| Evento                                                                                                | Descrição                                                                                |
|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**MSFT \_ WmiProviderEvent**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiproviderevent)                               | Classe pai para todos os eventos do provedor de consumidor.                                  |
| [**MSFT \_ WmiConsumerProviderLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderloaded)             | Define a ativação bem-sucedida do objeto COM do provedor de consumidor de eventos.    |
| [**MSFT \_ WmiConsumerProviderUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerproviderunloaded)         | Define a desativação bem-sucedida do objeto COM do provedor de consumidor de eventos.  |
| [**MSFT \_ WmiConsumerProviderSinkLoaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkloaded)     | Define a ativação bem-sucedida do objeto de sink do provedor de eventos do consumidor.   |
| [**MSFT \_ WmiConsumerProviderSinkUnloaded**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiconsumerprovidersinkunloaded) | Define a desativação bem-sucedida do objeto de sink do provedor de eventos do consumidor. |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Solução de problemas de WMI](wmi-troubleshooting.md)
</dt> <dt>

Solução de problemas de WMI
</dt> <dt>

[Recebendo um evento WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
