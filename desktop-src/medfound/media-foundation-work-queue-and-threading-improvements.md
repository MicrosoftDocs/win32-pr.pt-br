---
description: Este tópico descreve as melhorias no Windows 8 para filas de trabalho e threading na plataforma Microsoft Media Foundation.
ms.assetid: 9E2A1D94-BF82-488E-8297-D524683ABE17
title: Aprimoramentos na fila de trabalho e threading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07b307cb00316696e075e9e9cc2a138e98e149be
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104011954"
---
# <a name="work-queue-and-threading-improvements"></a>Aprimoramentos na fila de trabalho e threading

Este tópico descreve as melhorias no Windows 8 para filas de trabalho e threading na plataforma Microsoft Media Foundation.

-   [Comportamento do Windows 7](#windows-7-behavior)
    -   [Filas de trabalho](#work-queues)
    -   [Suporte do MMCSS](#mmcss-support)
    -   [IMFRealTimeClient](#imfrealtimeclientex)
-   [Aprimoramentos do Windows 8](#windows-8-improvements)
    -   [Filas de trabalho multi-threaded](#multithreaded-work-queues)
    -   [Filas de trabalho da tarefa compartilhada](#shared-task-work-queues)
    -   [Aguardar fila](#wait-queue)
    -   [Aprimoramentos no suporte do MMCSS](#enhancements-to-mmcss-support)
    -   [IMFRealTimeClientEx](#imfrealtimeclientex)
    -   [Branches de topologia](#topology-branches)
-   [Recomendações](#recommendations)
-   [Resumo](#summary)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-7-behavior"></a>Comportamento do Windows 7

Esta seção resume o comportamento de Media Foundation filas de trabalho no Windows 7.

### <a name="work-queues"></a>Filas de trabalho

A plataforma Media Foundation cria várias filas de trabalho padrão. Somente dois são documentados como sendo usados para uso geral do aplicativo:

-   **padrão de fila de retorno de \_ chamada MFASYNC \_ \_**
-   **\_ \_ função longa da fila de retorno de chamada MFASYNC \_ \_**

Um aplicativo ou componente pode alocar novas filas de trabalho chamando [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) ou [**MFAllocateWorkQueueEx**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueueex). A função **MFAllocateWorkQueueEx** define dois tipos de fila de trabalho:

-   **MF \_ A \_** fila de trabalhos padrão cria uma fila de trabalho sem um loop de mensagem.
-   **MF \_ A janela \_ fila** cria uma fila de trabalho com um loop de mensagem.

Para enfileirar um item de trabalho, chame [**MFPutWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem) ou [**MFPutWorkItemEx**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex). A plataforma executa o item de trabalho invocando a implementação fornecida pelo chamador de [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback). No Windows 7 e versões anteriores, a plataforma cria um thread por fila de trabalho.

### <a name="mmcss-support"></a>Suporte do MMCSS

O [serviço do Agendador de classes de multimídia](../procthread/multimedia-class-scheduler-service.md) (MMCSS) gerencia prioridades de thread para que os aplicativos de multimídia obtenham fatias regulares de tempo de CPU, sem negar recursos de CPU a aplicativos de prioridade mais baixa. O MMCSS define um conjunto de *tarefas* que têm perfis de utilização de CPU diferentes. Quando um thread ingressa em uma tarefa do MMCSS, o MMCSS define a prioridade do thread com base em vários fatores:

-   A prioridade base da tarefa, que é definida no registro.
-   A prioridade de thread relativa, que é definida em tempo de execução chamando [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).
-   Várias características de tempo de execução, como se o aplicativo está em primeiro plano e quanto tempo de CPU está sendo consumido pelos threads em cada classe do MMCSS.

Um aplicativo pode registrar uma fila de trabalho com o MMCSS chamando [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss). Essa função usa uma ID de fila de trabalho, uma classe do MMCSS (nome da tarefa) e o identificador de tarefa do MMCSS. Internamente, ele chama [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) com o nome da tarefa e a ID da tarefa. Depois que uma fila de trabalho é registrada com o MMCSS, você pode obter a ID da classe e da tarefa chamando [**MFGetWorkQueueMMCSSClass**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcssclass) e [**MFGetWorkQueueMMCSSTaskId**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsstaskid).

A [sessão de mídia](media-session.md) fornece um acesso de nível mais alto a essas APIs, por meio da interface [**IMFWorkQueueServices**](/windows/desktop/api/mfidl/nn-mfidl-imfworkqueueservices) . Essa interface fornece dois métodos principais:

| Método                                                                                                            | Descrição                                                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss)   | Registra uma fila de trabalho com uma tarefa do MMCSS. Esse método é essencialmente um wrapper fino em volta de [**MFBeginRegisterWorkQueueWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcss), mas você pode passar o valor **MFASYNC \_ fila de retorno de chamada \_ \_** para registrar todas as filas de trabalho da plataforma de uma vez. |
| [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) | Registra uma ramificação da topologia com uma fila de trabalho.                                                                                                                                                                                                                                         |



 

Para registrar uma ramificação de topologia, faça o seguinte.

1.  Defina o atributo de ID de fila de TOPONODE do MF no nó de origem para a ramificação. [ \_ \_ \_ ](mf-toponode-workqueue-id-attribute.md) Use qualquer valor definido pelo aplicativo.
2.  Opcionalmente, defina a **\_ classe MF TOPONODE Queue \_ \_ MMCSS \_** para unir a fila de trabalho a uma tarefa do MMCSS.
3.  Chame [**BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) na topologia resolvida.

A sessão de mídia aloca uma nova fila de trabalho para cada valor exclusivo da [ \_ ID de \_ fila \_ de filas MF TOPONODE](mf-toponode-workqueue-id-attribute.md). Para cada ramificação de topologia, as operações de pipeline assíncronas são executadas na fila de trabalho que é atribuída à ramificação.

### <a name="imfrealtimeclient"></a>IMFRealTimeClient

A interface [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient) é destinada a componentes de pipeline que criam seus próprios threads ou usam filas de trabalho para operações assíncronas. A sessão de mídia usa essa interface para notificar o componente de pipeline do comportamento correto, da seguinte maneira:

-   Se o componente de pipeline criar um thread de trabalho, o método [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads) notificará o componente que a classe do MMCSS deve ingressar.
-   Se o componente de pipeline usa uma fila de trabalho, o método [**IMFRealTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue) informa o componente que a fila de trabalho deve usar.

Normalmente, um componente de pipeline usa um thread ou uma fila de trabalho para executar tarefas assíncronas, mas não ambos.

## <a name="windows-8-improvements"></a>Aprimoramentos do Windows 8

### <a name="multithreaded-work-queues"></a>Filas de trabalho multi-threaded

No Windows 8, o Media Foundation dá suporte a um novo tipo de fila de trabalho chamado *fila multi-threaded*. Uma fila multi-threaded usa um pool de segmentos do sistema para distribuir itens de trabalho. A fila multi-threaded escala melhor do que as filas de thread único anteriores. Por exemplo,

-   Vários componentes podem compartilhar uma fila multi-threaded sem bloquear um ao outro, exigindo a criação de menos threads.

-   Os itens de trabalho são otimizados para evitar alternâncias de contexto se um evento já estiver definido. Isso é mais eficiente do que criar seus próprios threads para aguardar eventos.

Ao usar o [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex), os aplicativos devem evitar a rotação de threads e, em vez disso, devem usar as filas de trabalho. Para fazer isso, os aplicativos devem implementar [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex) e não usar [**RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) e [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads).

Quando a plataforma de Media Foundation é inicializada, ela cria uma fila multi-threaded com a fila de retorno de chamada MFASYNC do identificador com **\_ \_ \_ vários threads**.

Uma fila multi-threaded não serializa itens de trabalho. Sempre que um thread do pool de threads se tornar disponível, o próximo item de trabalho na fila será expedido. O chamador deve garantir que o trabalho seja serializado corretamente. Para tornar isso mais fácil, Media Foundation define uma *fila de trabalho serial*. Uma fila serial encapsula outra fila de trabalho, mas garante a execução totalmente serializada. O próximo item na fila não é expedido até que o item anterior seja concluído.

O código a seguir cria uma fila de serializador na fila multithread de plataforma.


```C++
DWORD workQueueID;
hr = MFAllocateSerialWorkQueue(MFASYNC_CALLBACK_QUEUE_MULTITHREADED, &workQueueID); 
```



Mais de uma fila serial pode encapsular a mesma fila multi-threaded. Em seguida, as filas de série compartilham o mesmo pool de threads e a execução serializada é imposta dentro de cada fila.

As filas de trabalho padrão que existiam antes do Windows 8 agora são implementadas como filas de trabalho seriais que encapsulam a fila multi-threaded de plataforma. Essa alteração preserva a compatibilidade com versões anteriores.

### <a name="shared-task-work-queues"></a>Filas de trabalho da tarefa compartilhada

Para funcionar corretamente com o Agendador de kernel, deve haver uma fila de trabalho multi-threaded para cada tarefa do MMCSS que você usar. A plataforma Media Foundation aloca isso conforme necessário, até uma por tarefa do MMCSS, por processo. Para obter a fila de trabalho compartilhada para uma tarefa do MMCSS em particular, chame [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue) e especifique o nome da tarefa. A função pesquisa o nome da tarefa em uma tabela. Se uma fila de trabalho ainda não existir para essa tarefa, a função alocará uma nova fila de trabalho MT e a unirá imediatamente à tarefa do MMCSS. Se uma fila de trabalho já existir para essa tarefa, a função retornará o identificador da fila de trabalho existente.

### <a name="wait-queue"></a>Aguardar fila

A *fila de espera* é uma fila de trabalho de plataforma especial que aguarda eventos a serem sinalizados. Se um componente precisar aguardar que um evento seja sinalizado, ele poderá usar a fila de espera em vez de criar um thread de trabalho para aguardar o evento.

Para usar a fila de espera, chame [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem). Os parâmetros incluem o identificador de evento e um ponteiro [**IMFAsyncResult**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Quando o evento é sinalizado, a fila de espera invoca o retorno de chamada. Há uma única fila de espera de plataforma; os aplicativos não podem criar suas próprias filas de espera.

### <a name="enhancements-to-mmcss-support"></a>Aprimoramentos no suporte do MMCSS

As novas funções de plataforma de Media Foundation a seguir estão relacionadas ao MMCSS.



| Função                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex) | Registra uma fila de trabalho com o MMCSS. Essa função inclui um parâmetro para especificar a prioridade de thread relativa. Internamente, esse valor é convertido em uma chamada para [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).                                                                                                                                                                               |
| [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)                 | Consulta a prioridade de uma fila de trabalho.                                                                                                                                                                                                                                                                                                                                                                 |
| [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)                 | Registra todas as filas de trabalho da plataforma com uma tarefa do MMCSS. Essa função é semelhante ao método [**IMFWorkQueueServices:: BeginRegisterPlatformWorkQueueWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregisterplatformworkqueuewithmmcss) , mas pode ser usada sem criar uma instância da sessão de mídia. Além disso, a função inclui um parâmetro para especificar a prioridade de thread base. |



 

Os aplicativos que usam a sessão de mídia devem definir o atributo de [ \_ classe MF TOPONODE \_ fila do \_ MMCSS \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) como "áudio" para a ramificação de renderização de áudio. Defina o atributo como "reprodução" para a ramificação de renderização de vídeo.

### <a name="imfrealtimeclientex"></a>IMFRealTimeClientEx

A interface [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex) substitui IMFRealTimeClient, para componentes de pipeline que executam operações assíncronas.



| Método                                                             | Descrição                                                                                                                                                                                                                    |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RegisterThreadsEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-registerthreadsex) | Notifica o componente para registrar seus threads com o MMCSS. Esse método é equivalente a [**IMFRealTimeClient:: RegisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-registerthreads), mas adiciona um parâmetro para a prioridade de thread base. |
| [**SetWorkQueueEx**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-setworkqueueex)       | Notifica o componente para usar uma fila de trabalho específica. Esse método é equivalente a [**IMFReadTimeClient:: SetWorkQueue**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-setworkqueue), mas adiciona um parâmetro para a prioridade de item de trabalho.               |
| [**UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclientex-unregisterthreads) | Notifica o componente para cancelar o registro de seus threads do MMCSS. Esse método é idêntico ao método [**IMFRealTimeClient:: UnregisterThreads**](/windows/desktop/api/mfidl/nf-mfidl-imfrealtimeclient-unregisterthreads) .                                       |



 

Os componentes de pipeline devem usar filas de trabalho e não devem criar threads de trabalho, pelos seguintes motivos:

-   As filas de trabalho são melhor dimensionadas, pois usam os pools de threads do sistema operacional.
-   A plataforma manipula os detalhes do registro de filas de trabalho com o MMCSS.
-   Um thread de trabalho pode facilmente causar um deadlock que é difícil de depurar.

Além disso, considere o uso da fila de trabalho do serializador se você precisar serializar suas operações assíncronas.

### <a name="topology-branches"></a>Branches de topologia

Se o atributo da [ \_ \_ \_ \_ classe MF TOPONODE Queue MMCSS](mf-toponode-workqueue-mmcss-class-attribute.md) registrar uma ramificação de topologia com o MMCSS, no Windows 8, a sessão de mídia USARá as filas de trabalho MT compartilhadas. Em versões anteriores do Windows, a sessão de mídia alocou uma nova fila de trabalho.

Dois novos atributos são definidos para registrar uma ramificação de topologia com o MMCSS.



| Atributo                                                                            | Descrição                         |
|--------------------------------------------------------------------------------------|-------------------------------------|
| [prioridade do TOPONODE de fila do MF do \_ \_ \_ MMCSS \_](mf-toponode-workqueue-mmcss-priority.md) | Especifica a prioridade de thread base. |
| [\_prioridade de \_ item de fila de TOPONODE MF \_ \_](mf-toponode-workqueue-item-priority.md)   | Especifica a prioridade do item de trabalho.   |



 

## <a name="recommendations"></a>Recomendações

-   Os aplicativos que usam a sessão de mídia devem definir a [ \_ classe MF TOPONODE \_ fila \_ \_ ](mf-toponode-workqueue-mmcss-class-attribute.md) de execução do MMCSS como "áudio" para a ramificação de renderização de áudio e "reprodução" para a ramificação de renderização de vídeo.
-   Os aplicativos que usam a sessão de mídia devem chamar [**IMFWorkQueueServices:: BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) na topologia.
-   Para componentes de pipeline, as filas de trabalho são recomendadas em vez de threads de trabalho. Se o componente usar filas de trabalho ou threads de trabalho, implemente [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex).
-   Não crie filas de trabalho particulares, pois isso anula a finalidade das filas de trabalho da plataforma. Use a fila multi-threaded da plataforma ou uma fila serial que encapsula a fila multi-threaded da plataforma.
-   Se você precisar serializar operações assíncronas, use uma fila serial.

## <a name="summary"></a>Resumo

As seguintes Media Foundation APIs de plataforma relacionadas a threads e filas de trabalho são novas para o Windows 8.

-   [\_prioridade de \_ item de fila de TOPONODE MF \_ \_](mf-toponode-workqueue-item-priority.md)
-   [prioridade do TOPONODE de fila do MF do \_ \_ \_ MMCSS \_](mf-toponode-workqueue-mmcss-priority.md)
-   [**MFAllocateSerialWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateserialworkqueue)
-   [**MFBeginRegisterWorkQueueWithMMCSSEx**](/windows/desktop/api/mfapi/nf-mfapi-mfbeginregisterworkqueuewithmmcssex)
-   [**MFGetWorkQueueMMCSSPriority**](/windows/desktop/api/mfapi/nf-mfapi-mfgetworkqueuemmcsspriority)
-   [**MFPutWaitingWorkItem**](/windows/desktop/api/mfapi/nf-mfapi-mfputwaitingworkitem)
-   [**MFPutWorkItem2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitem2)
-   [**MFPutWorkItemEx2**](/windows/desktop/api/mfapi/nf-mfapi-mfputworkitemex2)
-   [**MFRegisterPlatformWithMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfregisterplatformwithmmcss)
-   [**MFUnregisterPlatformFromMMCSS**](/windows/desktop/api/mfapi/nf-mfapi-mfunregisterplatformfrommmcss)
-   [**MFLockSharedWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mflocksharedworkqueue)
-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Filas de trabalho](work-queues.md)
</dt> </dl>

 

 
