---
description: Um provedor de consumidor de eventos é um componente da arquitetura de consumidor permanente que determina qual consumidor de evento permanente trata de um determinado evento.
ms.assetid: c5a0d0ec-99af-4815-9ad2-e59db70e04ce
ms.tgt_platform: multiple
title: Escrevendo um provedor de consumidor de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 312e0c2ecbf02d8bb0a8f491339d191aadde41a66cd3e3228c3187d5dcf689e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553093"
---
# <a name="writing-an-event-consumer-provider"></a>Escrevendo um provedor de consumidor de eventos

Um provedor de consumidor de eventos é um componente da arquitetura de consumidor permanente que determina qual consumidor de evento permanente trata de um determinado evento. Você deve criar um provedor de consumidor de eventos junto com seus consumidores de evento permanentes para rotear eventos adequadamente do WMI.

Um provedor de consumidor de eventos vincula um provedor de eventos a uma lista de classes de consumidor. As instâncias dessas classes de consumidor recebem eventos desse provedor. O WMI identifica a qual provedor de consumidor os eventos são entregues, com base na instância [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) , que associa a instância [**\_ \_ Win32Provider**](--win32provider.md) do provedor de consumidor a uma classe de consumidor lógica. Os usuários criam instâncias da classe consumidor como parte de uma assinatura permanente. Se o provedor de eventos não estiver em execução quando um evento ocorrer, o WMI iniciará o provedor quando precisar entregar eventos.

O procedimento a seguir descreve como implementar um provedor de consumidor de eventos.

**Para implementar um provedor de consumidor de eventos**

1.  Crie classes de consumidor em formato MOF (MOF) e registre-as com o WMI. Para obter mais informações, consulte [Designing formato MOF (MOF) classes](designing-managed-object-format--mof--classes.md).

    Provedores de classe se registram com WMI criando uma instância do [**\_ \_ Win32Provider**](--win32provider.md) e uma classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) . Para obter mais informações, consulte [registrando um provedor de consumidor de eventos](registering-an-event-consumer-provider.md).

2.  Implemente a interface [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para seu provedor.

    O WMI usa [**IWbemProviderInit**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemproviderinit) para carregar e inicializar um provedor. Para obter mais informações, consulte [inicializando um provedor](initializing-a-provider.md).

    > [!Note]  
    > Os provedores de consumidor de eventos são altamente incentivados a usar o modelo de vários threads "both".

     

3.  Implemente a interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) para seu provedor.

    A interface [**IWbemEventConsumerProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemeventconsumerprovider) é a interface principal para um provedor de consumidor de eventos.

4.  Forneça um ou mais consumidores físicos para receber as mensagens de evento do WMI.

    Um consumidor físico é um objeto COM que representa um consumidor de evento permanente. Todos os consumidores físicos devem implementar a interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . Para obter mais informações, consulte [implementando um consumidor físico](implementing-a-physical-consumer.md).

 

 



