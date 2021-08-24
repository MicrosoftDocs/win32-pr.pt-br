---
description: A classe CDynamicOutputPin implementa um pino de saída que dá suporte a reconexões dinâmicas e alterações de formato.
ms.assetid: d2488fba-a653-4b6e-b786-ce95f9e20daa
title: Classe CDynamicOutputPin (Amfilter.h)
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
ms.openlocfilehash: 6e0b8903f83c372aa85bd1c41fb12ce9065798d79dc4dbd940df926a395f8bc9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119871796"
---
# <a name="cdynamicoutputpin-class"></a>Classe CDynamicOutputPin

A `CDynamicOutputPin` classe implementa um pino de saída que dá suporte a reconexões dinâmicas e alterações de formato.

Essa classe deriva da classe [**CBaseOutputPin**](cbaseoutputpin.md) e implementa a interface [**IPinFlowControl.**](/windows/desktop/api/Strmif/nn-strmif-ipinflowcontrol) Ele dá suporte a várias operações que são importantes para a criação dinâmica de grafo:

-   Reconexão dinâmica: o pino pode se desconectar e reconectar enquanto o filtro ainda está ativo (em pausa ou em execução).
-   Alteração de formato dinâmico: o pino pode negociar um novo tipo de mídia enquanto o filtro ainda está ativo, sem se reconectar.
-   Flow controle: o filtro de propriedade (ou um aplicativo) pode bloquear o fluxo de dados do pino sem interromper o filtro.

Para obter mais informações, consulte [Dynamic Graph Building](dynamic-graph-building.md).

O pino tem três estados possíveis: bloqueado, desbloqueado e pendente. No estado *pendente, o* pino está aguardando que alguma operação seja concluída em outro thread, antes que o pino alterna para o estado bloqueado. Embora o pino seja bloqueado, o filtro não pode entregar dados por meio do pino ou alterar a conexão do pino.

Para coordenar entre vários threads, o filtro de propriedade deve seguir determinadas regras. (Para obter mais informações sobre threads no grafo de filtro, consulte [Threads e seções críticas](threads-and-critical-sections.md).) Primeiro, o thread de streaming sempre deve chamar o método [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) antes de chamar qualquer um dos seguintes métodos:

-   [**CDynamicOutputPin::ChangeOutputFormat**](cdynamicoutputpin-changeoutputformat.md)
-   [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md)
-   [**CDynamicOutputPin::D ynamicReconnect**](cdynamicoutputpin-dynamicreconnect.md)
-   [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md)
-   [**CBaseOutputPin::D eliverEndOfStream**](cbaseoutputpin-deliverendofstream.md)
-   [**CBaseOutputPin::D eliverNewSegment**](cbaseoutputpin-delivernewsegment.md)
-   [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

Posteriormente, ele deve chamar o [**método CDynamicOutputPin::StopUsingOutputPin.**](cdynamicoutputpin-stopusingoutputpin.md)

Em segundo lugar, o thread do aplicativo não deve chamar nenhum dos métodos na lista anterior. Em terceiro lugar, o thread de streaming não deve chamar os métodos de classe que bloqueiam ou desbloqueia o pino. Esses métodos são: [**CDynamicOutputPin::Block**](cdynamicoutputpin-block.md), [**CDynamicOutputPin::SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md), [**CDynamicOutputPin::AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)e [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md).

Essas regras garantem que o thread do aplicativo não possa bloquear o pino enquanto o thread de streaming o estiver usando e vice-versa. Depois que o thread de streaming tiver chamado **StartUsingOutputPin**, o pino não será bloqueado até que o thread de streaming chamar **StopUsingOutputPin**. Por outro lado, se o pino estiver bloqueado, **StartUsingOutputPin** aguardará até que o pino seja desbloqueado.

Para evitar esquecer de chamar **StopUsingOutputPin**, você pode usar a [**classe CAutoUsingOutputPin.**](cautousingoutputpin-cautousingoutputpin.md) Ele chama **StopUsingOutputPin** automaticamente quando ele sai do escopo.

Quando o filtro de propriedade une ou deixa o grafo de filtro (em seu método [**IBaseFilter::JoinFilterGraph),**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph) ele deve chamar o método [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) do pino.



| Variáveis de membro protegidas                                                                      | Descrição                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md)                                 | Seção crítica que protege o estado de bloqueio.                                                                            |
| [**m \_ hUnblockOutputPinEvent**](cdynamicoutputpin-m-hunblockoutputpinevent.md)                 | Evento que é sinalizado quando o pino não está bloqueado.                                                                           |
| [**m \_ hNotifyCallerPinBlockedEvent**](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)     | Evento que é sinalizado quando o pino é bloqueado com êxito ou o usuário cancela um bloco pendente.                                 |
| [**m \_ BlockState**](cdynamicoutputpin-m-blockstate.md)                                         | Estado de bloqueio.                                                                                                               |
| [**m \_ dwBlockCallerThreadID**](cdynamicoutputpin-m-dwblockcallerthreadid.md)                   | O identificador do thread que chamou pela última vez [**o método IPinFlowControl::Block**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) nesse pino. |
| [**m \_ dwNumOutstandingOutputPinUsers**](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md) | Número de threads de streaming usando esse pino.                                                                                   |
| [**m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md)                                         | Evento que é sinalizado quando o filtro é interrompido ou o pino libera dados.                                                         |
| [**m \_ pGraphConfig**](cdynamicoutputpin-m-pgraphconfig.md)                                     | Ponteiro para a interface [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) para executar reconexões dinâmicas.                           |
| [**m \_ bPinUsesReadOnlyAllocator**](cdynamicoutputpin-m-bpinusesreadonlyallocator.md)           | Sinalizador que especifica se os exemplos do alocador do pino são somente leitura.                                                   |
| Métodos Protegidos                                                                               | Descrição                                                                                                                   |
| [**SynchronousBlockOutputPin**](cdynamicoutputpin-synchronousblockoutputpin.md)                | Bloqueia o pino; não retorna até que o pino seja bloqueado.                                                                     |
| [**AsynchronousBlockOutputPin**](cdynamicoutputpin-asynchronousblockoutputpin.md)              | Bloqueia o pino; pode retornar antes que o pino seja bloqueado.                                                                       |
| [**UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md)                                  | Desbloqueia o pino.                                                                                                             |
| [**BlockOutputPin**](cdynamicoutputpin-blockoutputpin.md)                                      | Bloqueia o pino.                                                                                                               |
| [**WaitEvent**](cdynamicoutputpin-waitevent.md)                                                | Aguarda até que o evento especificado seja sinalizado.                                                                                  |
| Métodos públicos                                                                                  | Descrição                                                                                                                   |
| [**CDynamicOutputPin**](cdynamicoutputpin-cdynamicoutputpin.md)                                | Método do construtor.                                                                                                           |
| [**~CDynamicOutputPin**](cdynamicoutputpin--cdynamicoutputpin.md)                              | Método destruidor.                                                                                                            |
| [**SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md)                                        | Especifica o ponteiro [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig) e o evento stop.                                                |
| [**DeliverBeginFlush**](cdynamicoutputpin-deliverbeginflush.md)                                | Solicita o pino de entrada conectado para iniciar uma operação de liberação.                                                                  |
| [**DeliverEndFlush**](cdynamicoutputpin-deliverendflush.md)                                    | Solicita o pino de entrada conectado para encerrar uma operação de liberação.                                                                    |
| [**Inativo**](cdynamicoutputpin-inactive.md)                                                  | Notifica o pino de que o filtro foi interrompido.                                                                                 |
| [**Ativo**](cdynamicoutputpin-active.md)                                                      | Notifica o pino de que o filtro agora está ativo.                                                                               |
| [**Completeconnect**](cdynamicoutputpin-completeconnect.md)                                    | Conclui uma conexão com um pino de entrada. Virtual.                                                                              |
| [**StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md)                            | Obtém acesso ao pin para uma operação de streaming. Virtual.                                                                 |
| [**StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md)                              | Libera o acesso ao pin após uma operação de streaming. Virtual.                                                              |
| [**StreamingThreadUsingOutputPin**](cdynamicoutputpin-streamingthreadusingoutputpin.md)        | Determina se algum thread está executando uma operação de streaming no pino. Virtual.                                        |
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
| parâmetro<br/>  | <dl> <dt>Amfilter. h (incluir Fluxos. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




