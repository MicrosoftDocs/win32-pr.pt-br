---
description: A classe CDynamicOutputPin implementa um pino de saída que dá suporte a reconexões dinâmicas e a alterações de formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Classe CDynamicOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 54c6dab41c122456076299df22bf90d886c905cc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752702"
---
# <a name="cdynamicoutputpin-class"></a>Classe CDynamicOutputPin

A `CDynamicOutputPin` classe implementa um pino de saída que dá suporte a reconexões dinâmicas e a alterações de formato.

Essa classe deriva da classe [**CBaseOutputPin**](cbaseoutputpin.md) e implementa a interface [**IPinFlowControl**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) . Ele dá suporte a várias operações que são importantes para a criação dinâmica de gráficos:

-   Reconexão dinâmica: o PIN pode se desconectar e reconectar enquanto o filtro ainda estiver ativo (em pausa ou em execução).
-   Alteração de formato dinâmico: o PIN pode negociar um novo tipo de mídia enquanto o filtro ainda estiver ativo, sem reconectar.
-   Controle de fluxo: o filtro proprietário (ou um aplicativo) pode bloquear o fluxo de dados do PIN sem parar o filtro.

Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md).

O PIN tem três estados possíveis: bloqueado, desbloqueado e pendente. No estado *pendente* , o PIN está aguardando que alguma operação seja concluída em outro thread, antes que o PIN alterne para o estado bloqueado. Embora o PIN seja bloqueado, o filtro não pode entregar dados por meio do PIN ou alterar a conexão do PIN.

Para coordenar entre vários threads, o filtro proprietário deve seguir determinadas regras. (Para obter mais informações sobre threads no grafo de filtro, consulte [threads and Critical Sections](threads-and-critical-sections.md).) Primeiro, o thread de streaming sempre deve chamar o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar qualquer um dos seguintes métodos:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin:: receber**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Depois disso, ele deve chamar o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .

Em segundo lugar, o thread do aplicativo não deve chamar nenhum dos métodos na lista anterior. Terceiro, o thread de streaming não deve chamar os métodos de classe que bloqueiam ou desbloqueiam o PIN. Esses métodos são: [**CDynamicOutputPin:: Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin:: SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin:: AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)e [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Essas regras garantem que o thread do aplicativo não possa bloquear o PIN enquanto o thread de streaming o estiver usando e vice-versa. Depois que o thread de streaming tiver chamado **StartUsingOutputPin**, o PIN não será bloqueado até que o thread de streaming chame **StopUsingOutputPin**. Por outro lado, se o PIN for bloqueado, o **StartUsingOutputPin** aguardará até que o PIN seja desbloqueado.

Para evitar esquecer de chamar **StopUsingOutputPin**, você pode usar a classe [**CAutoUsingOutputPin**](cautousingoutputpin-cautousingoutputpin.md) . Ele chama **StopUsingOutputPin** automaticamente quando sai do escopo.

Quando o filtro proprietário se une ou leaveds o grafo de filtro (em seu método [**IBaseFilter:: JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) ), ele deve chamar o método [**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) do PIN.



| Variáveis de membro protegido                                                                      | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**\_BlockStateLock m**](cdynamicoutputpin-m-blockstatelock.md)                                 | Seção crítica que protege o estado de bloqueio.                                                                            |
| [**\_hUnblockOutputPinEvent m**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento sinalizado quando o PIN não é bloqueado.                                                                           |
| [**\_hNotifyCallerPinBlockedEvent m**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento sinalizado quando o PIN é bloqueado com êxito ou o usuário cancela um bloco pendente.                                 |
| [**\_bloco de bloqueio m**](cdynamicoutputpin-m-blockstate.md)                                         | Estado de bloqueio.                                                                                                               |
| [**\_dwBlockCallerThreadID m**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | O identificador do thread que chamou por último o método [**IPinFlowControl:: Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) neste PIN. |
| [**\_dwNumOutstandingOutputPinUsers m**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Número de threads de streaming usando este pin.                                                                                   |
| [**\_hStopEvent m**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento sinalizado quando o filtro é interrompido ou o PIN libera os dados.                                                         |
| [**\_pGraphConfig m**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Ponteiro para a interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) para executar reconexões dinâmicas.                           |
| [**\_bPinUsesReadOnlyAllocator m**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Sinalizador que especifica se os exemplos do alocador do PIN são somente leitura.                                                   |
| Métodos Protegidos                                                                               | Descrição                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Bloqueia o PIN; Não retorna até que o PIN seja bloqueado.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Bloqueia o PIN; pode retornar antes de o PIN ser bloqueado.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Desbloqueia o PIN.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Bloqueia o PIN.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Aguarda até que o evento especificado seja sinalizado.                                                                                  |
| Métodos públicos                                                                                  | Descrição                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Método de construtor.                                                                                                           |
| [**~ CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Método destruidor.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Especifica o ponteiro [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e o evento stop.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Solicita que o PIN de entrada conectado inicie uma operação de liberação.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Solicita que o PIN de entrada conectado Finalize uma operação de liberação.                                                                    |
| [**Inativo**](cdynamicoutputpin-inactive.md)                                                  | Notifica o PIN de que o filtro foi interrompido.                                                                                 |
| [**Activo**](cdynamicoutputpin-active.md)                                                      | Notifica o PIN de que o filtro está ativo agora.                                                                               |
| [**CompleteConnect**](cdynamicoutputpin-completeconnect.md)                                    | Conclui uma conexão com um PIN de entrada. VirtuaisLUNs.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Obtém acesso ao PIN para uma operação de streaming. VirtuaisLUNs.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Libera o acesso ao Pin após uma operação de streaming. VirtuaisLUNs.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina se algum thread está executando uma operação de streaming no PIN. VirtuaisLUNs.                                        |
| [**ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)                              | Altera dinamicamente o tipo de mídia para a conexão e fornece novas informações de segmento.                                  |
| [**ChangeMediaType**](cdynamicoutputpin-changemediatype.md)                                    | Altera dinamicamente o tipo de mídia para a conexão.                                                                        |
| [**DynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)                                  | Executa uma reconexão dinâmica com um novo tipo de mídia.                                                                        |
| Métodos IPin                                                                                    | Descrição                                                                                                                   |
| [**Desconectar**](cdynamicoutputpin-disconnect.md)                                              | Interrompe a conexão do PIN atual.                                                                                            |
| Métodos IPinFlowControl                                                                         | Descrição                                                                                                                   |
| [**Bloquear**](cdynamicoutputpin-block.md)                                                        | Bloqueia ou desbloqueia o fluxo de dados do PIN.                                                                             |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




