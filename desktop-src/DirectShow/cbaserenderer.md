---
description: A classe CBaseRenderer é uma classe base para implementar filtros de renderizador.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Classe CBaseRenderer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e30bae52cf5a7eba642354d002173291cb7d38b3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753175"
---
# <a name="cbaserenderer-class"></a>Classe CBaseRenderer

![hierarquia de classe CBaseRenderer](images/rbase02.png)

A `CBaseRenderer` classe é uma classe base para implementar filtros de renderizador. Ele dá suporte a um PIN de entrada, implementado pela classe [**CRendererInputPin**](crendererinputpin.md) . Para usar essa classe, declare uma classe derivada que herda `CBaseRenderer` . No mínimo, a classe derivada deve implementar os seguintes métodos, que são declarados como virtuais puros na classe base:

-   [**CBaseRenderer:: CheckMediaType**](cbaserenderer-checkmediatype.md): aceita ou rejeita tipos de mídia propostas. O filtro chama esse método durante o processo de conexão do PIN.
-   [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md): renderiza um exemplo. O filtro chama esse método para cada exemplo que recebe durante a execução.

A classe base lida com alterações de estado e problemas de sincronização. Ele também Agenda amostras para renderização, embora não implemente nenhuma medida de controle de qualidade. A classe base também declara vários métodos "Handler". Esses são os métodos que o filtro chama em pontos específicos no processo de streaming. Eles não fazem nada na classe base, mas a classe derivada pode substituí-los. Na tabela a seguir, eles são listados sob o título métodos públicos: manipuladores.

O manipulador [**CBaseRenderer:: OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) merece menção especial. O filtro chamará esse método se receber uma amostra enquanto o filtro estiver em pausa. Isso pode ocorrer se o grafo mudar de parado para em pausa ou se o grafo for buscado enquanto estiver em pausa. Os renderizadores de vídeo normalmente usam o exemplo para exibir um quadro ainda. Quando o filtro alterna de em pausa para em execução, ele envia o mesmo exemplo para o método [**CBaseRenderer::D orendersample**](cbaserenderer-dorendersample.md) , como o primeiro exemplo no fluxo.

A `CBaseRenderer` classe expõe as interfaces **IMediaSeeking** e **IMediaPosition** por meio do objeto [**CRendererPosPassThru**](crendererpospassthru.md) . Ele passa todas as solicitações de busca para o próximo filtro upstream.

## <a name="scheduling"></a>Agendamento

Quando o filtro upstream chama o método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada para entregar um exemplo, o PIN passa essa chamada para o método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) do filtro. O filtro descarta o exemplo, o renderiza imediatamente ou o agenda para renderização.

Se o exemplo não tiver carimbos de data/hora ou se nenhum relógio de referência estiver disponível, o filtro renderizará o exemplo imediatamente. Caso contrário, o filtro chama o método [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) para determinar o que fazer. Por padrão, o exemplo é agendado com base em seus carimbos de data/hora. A classe derivada pode substituir **ShouldDrawSampleNow** para dar suporte ao controle de qualidade.

Para agendar um exemplo, o filtro chama o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) , que cria uma solicitação de aviso. O método [**Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) então é bloqueado até a hora agendada ou até o estado do filtro ser alterado. O bloqueio impede que o filtro upstream entregue mais amostras até que a amostra atual seja renderizada.

Quando o filtro upstream chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) para sinalizar o final do fluxo, o filtro envia um evento [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro. O filtro aguarda o tempo de parada do exemplo atual antes de enviar o evento.



| Variáveis de membro protegido                                                   | Descrição                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**\_bAbort m**](cbaserenderer-m-babort.md)                                  | Sinalizador que indica se a renderização deve ser interrompida e rejeitada mais amostras.                                                               |
| [**\_bEOS m**](cbaserenderer-m-beos.md)                                      | Sinalizador que indica se o fim do fluxo foi atingido.                                                                                  |
| [**\_bEOSDelivered m**](cbaserenderer-m-beosdelivered.md)                    | Sinalizador que indica se o filtro postou o evento de conclusão do EC \_ .                                                               |
| [**\_bInReceive m**](cbaserenderer-m-binreceive.md)                          | Sinalizador que indica se o filtro está processando uma chamada de **recebimento** .                                                                |
| [**\_bRepaintStatus m**](cbaserenderer-m-brepaintstatus.md)                  | Sinalizador que habilita ou desabilita os eventos redesenhados.                                                                                           |
| [**\_bStreaming m**](cbaserenderer-m-bstreaming.md)                          | Sinalizador que indica se o filtro está transmitindo dados.                                                                               |
| [**\_dwAdvise m**](cbaserenderer-m-dwadvise.md)                              | Identificador do evento de temporizador que agenda a renderização.                                                                                 |
| [**\_EndOfStreamTimer m**](cbaserenderer-m-endofstreamtimer.md)              | Timer-identificador de evento, para agendar \_ notificações completas do EC.                                                                      |
| [**\_evComplete m**](cbaserenderer-m-evcomplete.md)                          | Evento sinalizado quando uma transição de estado é concluída.                                                                             |
| [**\_InterfaceLock m**](cbaserenderer-m-interfacelock.md)                    | Bloqueio de estado de filtro.                                                                                                                      |
| [**\_ObjectCreationLock m**](cbaserenderer-m-objectcreationlock.md)          | Bloquear para proteger a criação de objetos dentro do filtro.                                                                              |
| [**\_pInputPin m**](cbaserenderer-m-pinputpin.md)                            | Ponteiro para o pino de entrada do filtro.                                                                                                      |
| [**\_pMediaSample m**](cbaserenderer-m-pmediasample.md)                      | Ponteiro para o exemplo de mídia atual.                                                                                                    |
| [**\_pPosition m**](cbaserenderer-m-pposition.md)                            | Objeto auxiliar para passar comandos de busca upstream.                                                                                           |
| [**\_pQSink m**](cbaserenderer-m-pqsink.md)                                  | Ponteiro para o objeto que recebe mensagens de controle de qualidade.                                                                           |
| [**\_RendererLock m**](cbaserenderer-m-rendererlock.md)                      | Bloqueio de streaming.                                                                                                                         |
| [**\_RenderEvent m**](cbaserenderer-m-renderevent.md)                        | Evento usado para agendar a renderização.                                                                                                       |
| [**n º de \_ sinalização m**](cbaserenderer-m-signaltime.md)                          | Hora de parada no exemplo atual.                                                                                                        |
| [**\_ThreadSignal m**](cbaserenderer-m-threadsignal.md)                      | Evento usado para liberar o thread de streaming.                                                                                             |
| Métodos públicos                                                               | Descrição                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Cancela o evento de timer que agenda a renderização. VirtuaisLUNs.                                                                              |
| [**CBaseRenderer**](cbaserenderer-cbaserenderer.md)                         | Método de construtor.                                                                                                                     |
| [**~ CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Método destruidor.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera os ponteiros de interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do filtro. VirtuaisLUNs. |
| [**GetPin**](cbaserenderer-getpin.md)                                       | Recupera um PIN. VirtuaisLUNs.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera o número de Pins. VirtuaisLUNs.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera os carimbos de data/hora de um exemplo. VirtuaisLUNs.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Posta um evento de [**exibição de EC \_ \_ alterado**](ec-display-changed.md) no Gerenciador de gráfico de filtro.                                          |
| [**PrepareReceive**](cbaserenderer-preparereceive.md)                       | Prepara para renderizar um exemplo. VirtuaisLUNs.                                                                                                   |
| [**Recebe**](cbaserenderer-receive.md)                                     | Recebe o próximo exemplo de mídia no fluxo. VirtuaisLUNs.                                                                                  |
| [**Aplicar**](cbaserenderer-render.md)                                       | Renderiza um exemplo. VirtuaisLUNs.                                                                                                              |
| [**ScheduleSample**](cbaserenderer-schedulesample.md)                       | Agenda um exemplo para renderização. VirtuaisLUNs.                                                                                              |
| [**SendNotifyWindow**](cbaserenderer-sendnotifywindow.md)                   | Notifica o filtro upstream do identificador da janela de vídeo.                                                                                |
| [**SendRepaint**](cbaserenderer-sendrepaint.md)                             | Envia um evento Repaint para o Gerenciador do grafo de filtro.                                                                                      |
| [**SetMediaType**](cbaserenderer-setmediatype.md)                           | Chamado quando o tipo de mídia do PIN é definido. VirtuaisLUNs.                                                                                       |
| [**SignalTimerFired**](cbaserenderer-signaltimerfired.md)                   | Limpa o identificador do temporizador usado para agendar a renderização.                                                                                 |
| [**SourceThreadCanWait**](cbaserenderer-sourcethreadcanwait.md)             | Mantém ou libera o thread de streaming. VirtuaisLUNs.                                                                                        |
| [**WaitForReceiveToComplete**](cbaserenderer-waitforreceivetocomplete.md)   | Aguarda a conclusão do método [**CBaseRenderer:: Receive**](cbaserenderer-receive.md) .                                               |
| [**WaitForRenderTime**](cbaserenderer-waitforrendertime.md)                 | Aguarda o tempo de apresentação do exemplo atual. VirtuaisLUNs.                                                                              |
| Métodos públicos: métodos acessadores                                             | Descrição                                                                                                                             |
| [**ClearPendingSample**](cbaserenderer-clearpendingsample.md)               | Libera o exemplo atual. VirtuaisLUNs.                                                                                                   |
| [**GetCurrentSample**](cbaserenderer-getcurrentsample.md)                   | Recupera o exemplo atual. VirtuaisLUNs.                                                                                                  |
| [**Getrealstate**](cbaserenderer-getrealstate.md)                           | Recupera o estado do filtro.                                                                                                             |
| [**GetRenderEvent**](cbaserenderer-getrenderevent.md)                       | Recupera o evento que agenda a renderização.                                                                                           |
| [**HaveCurrentSample**](cbaserenderer-havecurrentsample.md)                 | Determina se o filtro tem um exemplo. VirtuaisLUNs.                                                                                    |
| [**IsEndOfStream**](cbaserenderer-isendofstream.md)                         | Consulta se a notificação de fim de fluxo foi recebida.                                                                            |
| [**IsEndOfStreamDelivered**](cbaserenderer-isendofstreamdelivered.md)       | Consulta se o \_ evento EC Complete foi entregue ao Gerenciador do grafo de filtro.                                                  |
| [**Isstreaminging**](cbaserenderer-isstreaming.md)                             | Consulta se o filtro está transmitindo dados.                                                                                           |
| [**SetAbortSignal**](cbaserenderer-setabortsignal.md)                       | Define um sinalizador que indica se a renderização deve ser interrompida e rejeitada mais amostras.                                                       |
| [**SetRepaintStatus**](cbaserenderer-setrepaintstatus.md)                   | Habilita ou desabilita os eventos redesenhados.                                                                                                     |
| Métodos públicos: métodos de State-Change                                         | Descrição                                                                                                                             |
| [**Ativo**](cbaserenderer-active.md)                                       | Chamado quando o estado é alternado para em pausa ou em execução. VirtuaisLUNs.                                                                        |
| [**BeginFlush**](cbaserenderer-beginflush.md)                               | Inicia uma operação de liberação. VirtuaisLUNs.                                                                                                      |
| [**BreakConnect**](cbaserenderer-breakconnect.md)                           | Libera o pino de entrada de uma conexão. VirtuaisLUNs.                                                                                      |
| [**CheckReady**](cbaserenderer-checkready.md)                               | Consulta se uma transição de estado foi concluída.                                                                                         |
| [**CompleteConnect**](cbaserenderer-completeconnect.md)                     | Conclui a conexão do pino de entrada com outro PIN. VirtuaisLUNs.                                                                           |
| [**CompleteStateChange**](cbaserenderer-completestatechange.md)             | Determina se uma transição para o estado em pausa está concluída. VirtuaisLUNs.                                                               |
| [**EndFlush**](cbaserenderer-endflush.md)                                   | Finaliza uma operação de liberação. VirtuaisLUNs.                                                                                                        |
| [**Inativo**](cbaserenderer-inactive.md)                                   | Chamado quando o estado é alternado para parado. VirtuaisLUNs.                                                                                  |
| [**NotReady**](cbaserenderer-notready.md)                                   | Sinaliza que uma transição de estado ainda não foi concluída.                                                                                    |
| [**Ready**](cbaserenderer-ready.md)                                         | Sinaliza que uma transição de estado foi concluída.                                                                                            |
| [**StartStreaming**](cbaserenderer-startstreaming.md)                       | Inicia o streaming quando o filtro alterna para um estado de execução. VirtuaisLUNs.                                                               |
| [**StopStreaming**](cbaserenderer-stopstreaming.md)                         | Interrompe o streaming quando o filtro sai do estado de execução. VirtuaisLUNs.                                                             |
| Métodos públicos: métodos de fim de fluxo                                        | Descrição                                                                                                                             |
| [**EndOfStream**](cbaserenderer-endofstream.md)                             | Notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo. VirtuaisLUNs.                                                 |
| [**NotifyEndOfStream**](cbaserenderer-notifyendofstream.md)                 | Posta um evento do [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro.                                                         |
| [**ResetEndOfStream**](cbaserenderer-resetendofstream.md)                   | Redefine os sinalizadores de fim de fluxo.                                                                                                         |
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Cancela o timer que agenda as \_ notificações completas do EC. VirtuaisLUNs.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Se o fim do fluxo for atingido, o agendará um \_ evento de conclusão do EC para o Gerenciador do grafo de filtro. VirtuaisLUNs.                                    |
| [**TimerCallback**](cbaserenderer-timercallback.md)                         | Método de retorno de chamada para o evento de timer de fim de fluxo.                                                                                      |
| Métodos públicos: manipuladores                                                     | Descrição                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Chamado quando o filtro recebe um exemplo enquanto está em pausa. VirtuaisLUNs.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Chamado depois que um exemplo é renderizado. VirtuaisLUNs.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Chamado quando a renderização está prestes a ser iniciada. VirtuaisLUNs.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Chamado quando o filtro começa o streaming. VirtuaisLUNs.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Chamado quando o filtro para de streaming. VirtuaisLUNs.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Chamado quando o filtro é concluído aguardando o tempo de apresentação de um exemplo. VirtuaisLUNs.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo. VirtuaisLUNs.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Chamado antes de o filtro renderizar um exemplo. VirtuaisLUNs.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina como um exemplo é agendado para renderização. VirtuaisLUNs.                                                                            |
| Métodos virtuais puros                                                         | Descrição                                                                                                                             |
| [**CheckMediaType**](cbaserenderer-checkmediatype.md)                       | Determina se o filtro aceita um tipo de mídia específico.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Renderiza um exemplo.                                                                                                                       |
| Métodos IMediaFilter                                                         | Descrição                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Recupera o estado do filtro (em execução, parado ou pausado).                                                                             |
| [**Pausar**](cbaserenderer-pause.md)                                         | Pausa o filtro.                                                                                                                      |
| [**Executar**](cbaserenderer-run.md)                                             | Executa o filtro.                                                                                                                        |
| [**Stop**](cbaserenderer-stop.md)                                           | Interrompe o filtro.                                                                                                                       |
| Métodos IBaseFilter                                                          | Descrição                                                                                                                             |
| [**FindPin**](cbaserenderer-findpin.md)                                     | Recupera o PIN com o identificador especificado.                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase. h (incluir fluxos. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt> </dl> |



 

 




