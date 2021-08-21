---
description: Um provedor de eventos pode dedicar bastante tempo para a criação de eventos.
ms.assetid: 5cf414f0-b3a8-4623-9aaa-08e2a28b40c0
ms.tgt_platform: multiple
title: Otimizando um provedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 613fa6b054f979d0f7d1a33a87f927df9ef129a280cf7cd1675cbe0cf9818473
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117923403"
---
# <a name="optimizing-an-event-provider"></a>Otimizando um provedor de eventos

Um provedor de eventos pode dedicar bastante tempo para a criação de eventos. Se nenhum aplicativo cliente usar os eventos criados, o provedor estará desperdiçando recursos do sistema. Além disso, o WMI gasta uma quantidade considerável de recursos analisando e enviando consultas complexas para o provedor apropriado. Para evitar o desperdício de recursos do sistema e melhorar o desempenho do seu provedor de eventos, você pode implementar a interface [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink) . O **IWbemEventProviderQuerySink** monitora as consultas que os aplicativos cliente registram com o WMI usando os métodos [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) e [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) . Ao monitorar as consultas de cliente registradas, seu provedor pode determinar e se qualquer mensagem deve ser enviada ao WMI.

O WMI chama [**NewQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-newquery) em um provedor de eventos quando um consumidor cliente registra uma consulta de filtro de eventos que contém referências a eventos com suporte pelo provedor de eventos. Portanto, o provedor de eventos responsável por eventos de modificação de instância para a classe **EmailClass** pode ser configurado para gerar notificações somente para o **remetente**. Quando o provedor recebe uma consulta solicitando a notificação de alterações para a propriedade **Subject** , o provedor pode começar a gerar essas notificações. Nesse cenário, o WMI não é necessário para descartar as notificações que relatam apenas as alterações de **destinatário** .

Da mesma forma, o WMI chama [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery) em um provedor de eventos quando um consumidor de cliente cancela o registro de uma consulta de filtro de eventos que contém referências a eventos com suporte no provedor de eventos. A finalidade de **CancelQuery** é que o provedor de eventos atualize a lista de quais eventos devem ser enviados.

> [!Note]  
> Se seu provedor oferecer suporte a [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) e [**IWbemEventProviderQuerySink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventproviderquerysink), verifique se a implementação do método **IUnknown:: QueryInterface** retorna ponteiros para ambas as interfaces.

 

 

 



