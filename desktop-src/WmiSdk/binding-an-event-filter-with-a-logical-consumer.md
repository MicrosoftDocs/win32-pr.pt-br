---
description: Depois de criar o consumidor de evento lógico e o filtro de eventos, você deve vinculá-los, o que registra o consumidor lógico para receber a notificação sobre os eventos especificados pelo filtro.
ms.assetid: 2fc3d781-2b93-4e9e-90a1-1b975ab40a01
ms.tgt_platform: multiple
title: Ligando um filtro de eventos a um consumidor lógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e99f44c4b64b98877231b73543d8753c765c3219
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829724"
---
# <a name="binding-an-event-filter-with-a-logical-consumer"></a>Ligando um filtro de eventos a um consumidor lógico

Depois de criar o consumidor de evento lógico e o filtro de eventos, você deve vinculá-los, o que registra o consumidor lógico para receber a notificação sobre os eventos especificados pelo filtro.

O procedimento a seguir descreve como associar um filtro de eventos a um consumidor lógico.

**Para associar um filtro de eventos a um consumidor lógico**

1.  Crie uma instância da classe de sistema [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) no repositório WMI.

    A classe [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) é uma classe de associação que vincula a instância de filtro de eventos e a instância de consumidor lógica em conjunto pelas propriedades de referência do **filtro** e do **consumidor** . Para obter mais informações, consulte [declarando uma classe de associação](declaring-an-association-class.md).

2.  Defina a propriedade de **filtro** para a instância do filtro.
3.  Defina a propriedade **consumidor** como a instância do consumidor lógico.
4.  Defina a propriedade **DeliverSynchronously** para determinar o tipo de entrega que você deseja.

    A propriedade **DeliverSynchronously** determina quando o WMI fornece notificações de eventos de forma síncrona ou assíncrona. Definir essa propriedade como **true** solicita uma entrega síncrona. Use a entrega síncrona somente quando o consumidor permanente puder processar eventos dentro de aproximadamente 100 microssegundos.

    > [!Note]  
    > Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

     

5.  Ao cancelar o registro de seu consumidor de evento lógico, certifique-se de excluir a instância [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) .

    Cada instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) representa um registro para uma notificação de evento específica. Quando você exclui uma associação, o WMI desativa o registro. Talvez seja necessário excluir as instâncias lógicas de consumidor e de filtro de eventos para desativar o registro, dependendo da implementação.

O exemplo de código a seguir mostra uma instância de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md) que associa uma instância de uma classe [**ActiveScriptEventConsumer**](activescripteventconsumer.md) a um filtro de eventos específico (a instância do consumidor de eventos foi criada no tópico [criando um consumidor lógico](creating-a-logical-consumer.md) e o filtro de eventos foi criado no tópico [criando um filtro de eventos](creating-an-event-filter.md) ).

``` syntax
instance of __FilterToConsumerBinding
{
    Filter = $FILTER;
    Consumer = $CONSUMER;
    DeliverSynchronously=FALSE;

    // this is the Administrators SID in array of bytes format
    CreatorSID = {1,2,0,0,0,0,0,5,32,0,0,0,32,2,0,0}; 
};
```

Dois consumidores, [**ActiveScriptEventConsumer**](activescripteventconsumer.md) e [**CommandLineEventConsumer**](commandlineeventconsumer.md), não funcionarão, a menos que seu criador seja membro do grupo local de administradores.

**:** Quando um administrador cria uma assinatura, seu SID não é usado para a propriedade **CreatorSID** , mas o SID do grupo de Administradores local é usado em vez disso. Portanto, as instâncias podem ser criadas por administradores diferentes e a assinatura ainda funcionará. Para obter mais informações, consulte [recebendo eventos com segurança](receiving-events-securely.md).

Quando um filtro é associado a um consumidor lógico, o evento é registrado pelo ETW ( [rastreamento de eventos](/windows/desktop/ETW/event-tracing-portal) para Windows). Para obter mais informações, consulte [rastreando a atividade WMI](tracing-wmi-activity.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recebendo eventos em todos os momentos](receiving-events-at-all-times.md)
</dt> </dl>

 

 
