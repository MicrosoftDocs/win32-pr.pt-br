---
description: Um consumidor físico é um objeto COM que implementa a interface IWbemUnboundObjectSink.
ms.assetid: 497457dc-61ca-4527-89fd-2af0383de5e9
ms.tgt_platform: multiple
title: Implementando um consumidor físico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0a9530ed7a98ce19b3b39f2f5a1fe52f3b0631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105814431"
---
# <a name="implementing-a-physical-consumer"></a>Implementando um consumidor físico

Um consumidor físico é um objeto COM que implementa a interface [**IWbemUnboundObjectSink**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemunboundobjectsink) . O WMI carrega seu consumidor físico e passa eventos por meio de **IWbemUnboundObjectSink** em resposta a um ou mais eventos, conforme definido pelo consumidor lógico associado. Os consumidores permanentes têm requisitos de segurança especiais. Para obter mais informações, consulte [SECURING WMI Events](securing-wmi-events.md).

O procedimento a seguir descreve como implementar um consumidor físico para um consumidor de evento permanente.

**Para implementar um consumidor físico para um consumidor de evento permanente**

1.  Crie um objeto COM.

    Você deve implementar um consumidor físico como um servidor local ou remoto usando o protocolo COM.

2.  Determine se você deseja dar suporte à notificação de eventos síncrona ou assíncrona.

    Com a notificação de eventos assíncronos, o thread de envio não está relacionado ao thread de recebimento. Portanto, nem o WMI nem o provedor de eventos são bloqueados enquanto o WMI entrega uma notificação para qualquer consumidor registrado para receber o evento. A desvantagem da entrega assíncrona é que uma alternância de contexto ocorre entre a hora em que o provedor produz o evento e a hora em que o consumidor recebe o evento. Para obter mais informações sobre como trabalhar de forma assíncrona, consulte o tópico [fundamentos do com](../com/guide.md) na seção com do SDK (Software Development Kit) do Microsoft Windows. Para obter mais informações sobre alternâncias de contexto, consulte o tópico [alternâncias de contexto](../procthread/context-switches.md) na seção DLLs, processos e threads do SDK do Windows.

    > [!Note]  
    > Como o retorno de chamada para o coletor pode não ser retornado no mesmo nível de autenticação que o cliente requer, é recomendável que você use semisynchronous em vez de comunicação assíncrona. Para obter mais informações, consulte [chamando um método](calling-a-method.md).

     

    Com a notificação síncrona, o WMI entrega a notificação no mesmo thread que o provedor de eventos usou para entregar o evento ao WMI. Nesse caso, quando um provedor de eventos envia uma notificação, o provedor de eventos é bloqueado pelo WMI até que o WMI forneça a notificação. Somente se o seu consumidor for extremamente rápido e puder processar um evento em 100 microssegundos ou menos, você considerará o suporte à notificação síncrona. Os consumidores síncronos que levam muito tempo para processar eventos podem prejudicar seriamente a entrega de eventos a todos os outros consumidores. Além disso, eles podem bloquear inadvertidamente o provedor. Para obter mais informações, consulte [associando um filtro de eventos a um consumidor lógico](binding-an-event-filter-with-a-logical-consumer.md).

3.  Implemente a função [**IWbemUnboundObjectSink:: IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) .

    O WMI usa a função [**IndicateToConsumer**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemunboundobjectsink-indicatetoconsumer) para passar os ponteiros e eventos necessários para o consumidor físico para comunicações síncronas e assíncronas. Sua implementação de **IndicateToConsumer** deve conter todo o código necessário para responder a um evento.

    Ao contrário de um consumidor de evento temporário, você não precisa chamar a interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) para entrar em contato com o WMI. Em vez disso, o WMI localiza um ponteiro para o consumidor por meio do provedor de consumidor de eventos. Para obter mais informações, consulte [escrevendo um provedor de consumidor de eventos](writing-an-event-consumer-provider.md).

    No entanto, se você quiser chamar novamente o WMI, use as interfaces [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) e [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) . O método tradicional para se conectar ao WMI é durante o processo de inicialização do seu objeto COM. Para obter mais informações, consulte [criando um aplicativo ou script WMI](creating-a-wmi-application-or-script.md).

    Se você implementar o consumidor físico como um servidor COM em processo e se conectar ao WMI separadamente do processo de inicialização, deverá usar o identificador de classe **\_ WbemAdministrativeLocator do CLSID** para acessar a interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) na chamada para [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).

    O exemplo a seguir mostra como usar o identificador de classe **\_ WbemAdministrativeLocator do CLSID** para acessar a interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) .

    ```C++
    IWbemLocator *pLoc = 0;

    DWORD dwRes = CoCreateInstance(CLSID_WbemAdministrativeLocator, 0, 
        CLSCTX_INPROC_SERVER, IID_IWbemLocator, (LPVOID *) &pLoc);
    ```

    

    A interface [**IWbemLocator**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemlocator) Obtém o ponteiro de namespace inicial para o WMI em um computador host específico. A falha ao usar o identificador **\_ WbemAdministrativeLocator do CLSID** na chamada [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) resulta em um erro de "acesso negado".

    Em circunstâncias usuais, o WMI fornece eventos assíncronos para o cliente, um de cada vez. No entanto, se um cliente não puder receber notificações de evento assíncrono tão rápido quanto os eventos chegarem, o WMI começará a enviar eventos em lote automaticamente em uma única chamada. O envio em lote automático ajuda se os tempos de ida e volta são um problema, como geralmente é o caso em cenários de alta taxa de transferência. No entanto, o envio em lote não melhora o desempenho do sistema se o cliente ou a largura de banda da rede estiverem em falha.

 

 
