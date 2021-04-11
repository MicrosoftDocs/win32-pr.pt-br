---
description: Talvez você queira escrever um aplicativo que possa reagir a eventos a qualquer momento.
ms.assetid: 475dca47-b1e5-4362-ab00-9ab9383e92f9
ms.tgt_platform: multiple
title: Recebendo eventos em todos os momentos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5559068e1e108c6f4185c31f8858a9e4169c50c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296595"
---
# <a name="receiving-events-at-all-times"></a>Recebendo eventos em todos os momentos

Talvez você queira escrever um aplicativo que possa reagir a eventos a qualquer momento. Por exemplo, um administrador pode querer receber uma mensagem de email quando medidas de desempenho específicas são recusadas em servidores de rede. Nesse caso, seu aplicativo deve ser executado o tempo todo. No entanto, a execução contínua de um aplicativo não é um uso eficiente dos recursos do sistema. Em vez disso, o WMI permite que você crie um consumidor de evento permanente. Os consumidores de eventos permanentes devem atender aos requisitos de segurança especiais. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).

Um consumidor de evento permanente recebe eventos até que seu registro seja explicitamente cancelado.

Um consumidor de evento permanente é uma combinação das seguintes classes, filtros e objetos COM do WMI que residem em seu sistema:

-   Um objeto COM chamado consumidor físico. O WMI fornece vários consumidores permanentes padrão. Por exemplo, o consumidor de evento de script ativo [executa um script quando ocorre um evento](running-a-script-based-on-an-event.md).
-   Uma nova classe de consumidor permanente.
-   Uma instância da classe de consumidor permanente chamada de consumidor lógico.
-   Um filtro que contém a consulta de eventos.
-   Uma ligação entre o consumidor e o filtro.

As propriedades de um consumidor de evento lógico especificam as ações a serem executadas quando notificado de um evento, mas não definem as consultas de evento com as quais elas estão associadas. Quando sinalizado, o WMI carrega automaticamente o objeto COM que representa o consumidor de evento permanente na memória ativa. Normalmente, isso ocorre durante a inicialização ou em resposta a um evento de disparo. Depois de ser ativado, o consumidor de evento permanente atua como um consumidor de evento normal, mas permanece até ser especificamente descarregado pelo sistema operacional.

Você pode escrever seu próprio consumidor de eventos permanentes ou usar as classes de [consumidor padrão](standard-consumer-classes.md)pré-instaladas do WMI, como [**ActiveScriptEventConsumer**](activescripteventconsumer.md). Para obter mais informações, consulte [classes de consumidor padrão](standard-consumer-classes.md), [monitorando e respondendo a eventos com consumidores padrão](monitoring-and-responding-to-events-with-standard-consumers.md)e [eventos de monitoramento](monitoring-events.md).

O procedimento a seguir descreve como criar seu próprio consumidor de evento permanente.

**Para criar seu próprio consumidor de evento permanente**

1.  Determine que tipo de eventos você deseja receber.

    O WMI dá suporte a eventos intrínsecos e extrínsecos. Um evento intrínseco é um evento predefinido pelo WMI, enquanto um evento extrínsecos é um evento definido por um provedor de terceiros. Para obter mais informações, consulte [determinando o tipo de evento a ser recebido](determining-the-type-of-event-to-receive.md).

2.  [Implemente um consumidor físico](implementing-a-physical-consumer.md).

    A principal diferença entre um aplicativo de gerenciamento e um [*consumidor físico*](gloss-p.md) é que um usuário carrega e descarrega um aplicativo de gerenciamento, enquanto o WMI carrega e descarrega um consumidor físico. A maior parte de sua codificação deve estar no consumidor físico.

    > [!Note]  
    > Esta etapa é primeiro no procedimento para facilitar a explicação. Em termos de codificação, você deve realmente criar o consumidor físico por último. Dessa forma, você pode dispor seus parâmetros e a lógica para seu provedor de eventos permanentes antes de iniciar a codificação demorada. No entanto, não há nenhuma restrição contra a gravação do consumidor físico primeiro.

     

3.  [Crie uma nova classe de consumidor descrevendo o consumidor físico](creating-a-new-permanent-event-consumer-class.md).

    Como qualquer classe, a classe consumidor descreve os parâmetros gerais de um consumidor de evento permanente para o WMI.

4.  [Crie uma instância da classe consumidor](creating-a-logical-consumer.md).

    Como qualquer outra classe WMI, você deve criar uma instância da classe consumidor se quiser implementar a classe. Uma instância de uma classe consumidor também é conhecida como [*consumidor lógico*](gloss-l.md). O consumidor lógico representa o consumidor físico para o WMI.

5.  [Crie um filtro de eventos](creating-an-event-filter.md).

    As consultas de evento que ativam os consumidores de eventos permanentes são chamadas de [*filtros de eventos*](gloss-e.md). Um único filtro de eventos pode ser associado a vários consumidores de eventos lógicos. Além disso, vários filtros de eventos podem ser associados a um único consumidor de evento lógico. O filtro é uma instância de [**\_ \_ EventFilter**](--eventfilter.md).

    Um evento de log do NT é gerado quando uma consulta do consumidor de evento permanente falha. A origem do evento é WinMgmt, a ID do evento é 10 e o tipo de evento é Error.

6.  [Vincule o filtro de eventos ao consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

    Ao vincular o filtro de eventos ao consumidor lógico, você instrui o WMI sobre qual filtro de eventos pertence a qual consumidor lógico. Os consumidores de eventos lógicos e os filtros de eventos são vinculados por uma instância de classe de associação de [**\_ \_ FilterToConsumerBinding**](--filtertoconsumerbinding.md). Quando é recebido um evento que corresponde a uma consulta de evento descrita em um filtro de eventos, o WMI localiza o consumidor de evento lógico associado examinando a instância da classe de associação. Depois que a instância do consumidor de evento lógico estiver localizada, o WMI usará uma instância da classe [**\_ \_ EventConsumerProviderRegistration**](--eventconsumerproviderregistration.md) para localizar e executar o consumidor de evento físico associado a essa instância.

7.  [Escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md).

    O provedor de consumidor de eventos é um objeto COM que localiza o consumidor físico para o WMI.

 

 



