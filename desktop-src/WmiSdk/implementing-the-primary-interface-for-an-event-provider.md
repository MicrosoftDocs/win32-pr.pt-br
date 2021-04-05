---
description: Um provedor de eventos deve implementar a interface IWbemEventProvider para gerar notificações de eventos.
ms.assetid: ae33c9f5-61f7-4488-a281-01d7f9c62c46
ms.tgt_platform: multiple
title: Implementando a interface primária para um provedor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5621a2c6d0901a7925828149dd5c1480c2b11456
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922200"
---
# <a name="implementing-the-primary-interface-for-an-event-provider"></a>Implementando a interface primária para um provedor de eventos

Um provedor de eventos deve implementar a interface [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) para gerar notificações de eventos. O WMI chama o método [**IWbemEventProvider::P rovideevents**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventprovider-provideevents) do provedor e passa um ponteiro para o objeto Sink, que é uma implementação da interface [**IWbemObjectSink**](iwbemobjectsink.md) . Quando o provedor de eventos estiver pronto para gerar uma notificação, o provedor chamará o método [**IWbemObjectSink:: indicativo**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) .

Um provedor de eventos deve posicionar as notificações geradas por meio de [**IWbemEventProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventprovider) em objetos de evento. Você deve implementar objetos de evento como entradas em uma matriz de interfaces [**IWbemClassObject**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemclassobject) representadas pelo parâmetro *ppObjArray* do método [**indique**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate) . Como **IWbemClassObjects** são objetos com, o provedor deve incrementar a contagem de referência para o coletor chamando o método [**IWbemObjectSink:: AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) . Provedores de eventos que devem fornecer muitas notificações (por exemplo, eventos 400) devem criar um objeto de evento exclusivo para cada notificação, gerando uma nova instância ou clonando uma existente. O WMI nunca se mantém em um objeto de evento após a conclusão da chamada de **indicação** e não tem requisitos especiais para **AddRef** acima e além do padrão com.

Considere as seguintes diretrizes ao implementar um provedor de eventos:

-   Não faça nenhuma alteração de classe durante a manutenção de uma chamada de cliente.
-   Não emita chamadas relacionadas a eventos, como uma chamada que modifica um filtro de eventos.
-   Processe todas as solicitações que o serviço de gerenciamento do Windows emite, como [**CancelQuery**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventproviderquerysink-cancelquery), antes de redisparar um evento.

    Se você não processar a solicitação, a reacionamento do evento poderá impedir que o evento seja aceito.

-   Nunca chame [**IWbemObjectSink:: SetStatus**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-setstatus) de dentro de um provedor.

 

 
