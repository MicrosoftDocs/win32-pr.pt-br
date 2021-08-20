---
description: A classe CBaseRenderer é uma classe base para implementar filtros de renderização.
ms.assetid: 8d39d3bd-6162-402e-a4b3-0f35d3e29b96
title: Classe CBaseRenderer (Renbase.h)
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
ms.openlocfilehash: 81e529493bfd892607748423bb1bab9016eb232aaeb3ed22287fa2c1c1917687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954796"
---
# <a name="cbaserenderer-class"></a>Classe CBaseRenderer

![Hierarquia de classes cbaserenderer](images/rbase02.png)

A `CBaseRenderer` classe é uma classe base para implementar filtros de renderização. Ele dá suporte a um pino de entrada, implementado pela [**classe CRendererInputPin.**](crendererinputpin.md) Para usar essa classe, declare uma classe derivada que herda `CBaseRenderer` . No mínimo, a classe derivada deve implementar os seguintes métodos, que são declarados como virtuais puros na classe base:

-   [**CBaseRenderer::CheckMediaType:**](cbaserenderer-checkmediatype.md)aceita ou rejeita os tipos de mídia propostos. O filtro chama esse método durante o processo de conexão de pino.
-   [**CBaseRenderer::D oRenderSample:**](cbaserenderer-dorendersample.md)renderiza um exemplo. O filtro chama esse método para cada amostra que recebe durante a execução.

A classe base lida com alterações de estado e problemas de sincronização. Ele também agenda exemplos para renderização, embora não implemente nenhuma medida de controle de qualidade. A classe base também declara vários métodos de "manipulador". Esses são métodos que o filtro chama em pontos específicos no processo de streaming. Eles não fazem nada na classe base, mas a classe derivada pode substituí-las. Na tabela a seguir, eles são listados sob o título Métodos Públicos: Manipuladores.

O [**manipulador CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md) não tem menção especial. O filtro chamará esse método se receber uma amostra enquanto o filtro estiver em pausa. Isso pode ocorrer se o grafo mudar de parado para pausado ou se o grafo for buscado enquanto está em pausa. Os renderadores de vídeo normalmente usam o exemplo para exibir um quadro parado. Quando o filtro muda de pausa para em execução, ele envia o mesmo exemplo para o método [**CBaseRenderer::D oRenderSample,**](cbaserenderer-dorendersample.md) como o primeiro exemplo no fluxo.

A `CBaseRenderer` classe expõe as interfaces **IMediaSeeking** e **IMediaPosition** por meio do [**objeto CRendererPosPassThru.**](crendererpospassthru.md) Ele passa todas as solicitações de busca para o próximo filtro upstream.

## <a name="scheduling"></a>Agendamento

Quando o filtro upstream chama o método [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do pino de entrada para fornecer um exemplo, o pino passa essa chamada para o método [**CBaseRenderer::Receive**](cbaserenderer-receive.md) do filtro. O filtro descarta o exemplo, renderiza-o imediatamente ou agenda-o para renderização.

Se o exemplo não tiver carimbos de data/hora ou se nenhum relógio de referência estiver disponível, o filtro renderizará o exemplo imediatamente. Caso contrário, o filtro chamará [**o método CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md) para determinar o que fazer. Por padrão, o exemplo é agendado com base em seus carimbos de data/hora. A classe derivada pode substituir **ShouldDrawSampleNow para** dar suporte ao controle de qualidade.

Para agendar um exemplo, o filtro chama o [**método IReferenceClock::AdviseTime,**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) que cria uma solicitação de consultoria. Em [**seguida, o método**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) Receive é bloco até a hora agendada ou até que o filtro mude de estado. O bloqueio impede que o filtro upstream entregue mais amostras até que a amostra atual seja renderizada.

Quando o filtro upstream chama o método [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) para sinalizar o final do fluxo, o filtro envia um evento [**EC \_ COMPLETE**](ec-complete.md) para o gerenciador de grafo de filtro. O filtro aguarda a hora de parada do exemplo atual antes de enviar o evento.



| Variáveis de membro protegidas                                                   | Descrição                                                                                                                             |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**m \_ bAbort**](cbaserenderer-m-babort.md)                                  | Sinalizador que indica se a renderização deve ser parada e rejeitar mais amostras.                                                               |
| [**m \_ bEOS**](cbaserenderer-m-beos.md)                                      | Sinalizador que indica se o fim do fluxo foi atingido.                                                                                  |
| [**m \_ bEOSDelivered**](cbaserenderer-m-beosdelivered.md)                    | Sinalizador que indica se o filtro postou o evento EC \_ COMPLETE.                                                               |
| [**m \_ bInReceive**](cbaserenderer-m-binreceive.md)                          | Sinalizador que indica se o filtro está processando uma **chamada receive.**                                                                |
| [**m \_ bRepaintStatus**](cbaserenderer-m-brepaintstatus.md)                  | Sinalizador que habilita ou desabilita eventos de repaint.                                                                                           |
| [**m \_ bStreaming**](cbaserenderer-m-bstreaming.md)                          | Sinalizador que indica se o filtro está transmitindo dados.                                                                               |
| [**m \_ dwAdvise**](cbaserenderer-m-dwadvise.md)                              | Identificador do evento de temporizador que agenda a renderização.                                                                                 |
| [**m \_ EndOfStreamTimer**](cbaserenderer-m-endofstreamtimer.md)              | Identificador de evento de temporizador, para agendar notificações EC \_ COMPLETE.                                                                      |
| [**m \_ evComplete**](cbaserenderer-m-evcomplete.md)                          | Evento que é sinalizado quando uma transição de estado é concluída.                                                                             |
| [**m \_ InterfaceLock**](cbaserenderer-m-interfacelock.md)                    | Bloqueio de estado de filtro.                                                                                                                      |
| [**m \_ ObjectCreationLock**](cbaserenderer-m-objectcreationlock.md)          | Bloqueie para proteger a criação de objetos dentro do filtro.                                                                              |
| [**m \_ pInputPin**](cbaserenderer-m-pinputpin.md)                            | Ponteiro para o pino de entrada do filtro.                                                                                                      |
| [**m \_ pMediaSample**](cbaserenderer-m-pmediasample.md)                      | Ponteiro para o exemplo de mídia atual.                                                                                                    |
| [**m \_ pPosition**](cbaserenderer-m-pposition.md)                            | Objeto auxiliar para passar comandos de busca upstream.                                                                                           |
| [**m \_ pQSink**](cbaserenderer-m-pqsink.md)                                  | Ponteiro para o objeto que recebe mensagens de controle de qualidade.                                                                           |
| [**m \_ RendererLock**](cbaserenderer-m-rendererlock.md)                      | Bloqueio de streaming.                                                                                                                         |
| [**m \_ RenderEvent**](cbaserenderer-m-renderevent.md)                        | Evento usado para agendar a renderização.                                                                                                       |
| [**m \_ SignalTime**](cbaserenderer-m-signaltime.md)                          | Hora de parada no exemplo atual.                                                                                                        |
| [**m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md)                      | Evento usado para liberar o thread de streaming.                                                                                             |
| Métodos públicos                                                               | Descrição                                                                                                                             |
| [**CancelNotification**](cbaserenderer-cancelnotification.md)               | Cancela o evento de temporizador que agenda a renderização. Virtual.                                                                              |
| [**Cbaserenderer**](cbaserenderer-cbaserenderer.md)                         | Método do construtor.                                                                                                                     |
| [**~CBaseRenderer**](cbaserenderer--cbaserenderer.md)                       | Método destruidor.                                                                                                                      |
| [**GetMediaPositionInterface**](cbaserenderer-getmediapositioninterface.md) | Recupera os ponteiros da interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) do filtro. Virtual. |
| [**Getpin**](cbaserenderer-getpin.md)                                       | Recupera um pino. Virtual.                                                                                                               |
| [**GetPinCount**](cbaserenderer-getpincount.md)                             | Recupera o número de pinos. Virtual.                                                                                                  |
| [**GetSampleTimes**](cbaserenderer-getsampletimes.md)                       | Recupera os carimbos de data/hora de um exemplo. Virtual.                                                                                       |
| [**OnDisplayChange**](cbaserenderer-ondisplaychange.md)                     | Posta um [**evento EC \_ DISPLAY \_ CHANGED**](ec-display-changed.md) no gerenciador de grafo de filtro.                                          |
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
| [**ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md)         | Cancela o timer que agenda as \_ notificações completas do EC. Virtual.                                                                   |
| [**SendEndOfStream**](cbaserenderer-sendendofstream.md)                     | Se o fim do fluxo for atingido, agendará um evento EC \_ COMPLETE para o gerenciador de grafo de filtro. Virtual.                                    |
| [**Timercallback**](cbaserenderer-timercallback.md)                         | Método de retorno de chamada para o evento de temporizador de fim de fluxo.                                                                                      |
| Métodos públicos: manipuladores                                                     | Descrição                                                                                                                             |
| [**OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)           | Chamado quando o filtro recebe um exemplo enquanto está em pausa. Virtual.                                                                         |
| [**OnRenderEnd**](cbaserenderer-onrenderend.md)                             | Chamado depois que um exemplo é renderizado. Virtual.                                                                                             |
| [**OnRenderStart**](cbaserenderer-onrenderstart.md)                         | Chamado quando a renderização está prestes a começar. Virtual.                                                                                       |
| [**OnStartStreaming**](cbaserenderer-onstartstreaming.md)                   | Chamado quando o filtro começa a transmitir. Virtual.                                                                                       |
| [**OnStopStreaming**](cbaserenderer-onstopstreaming.md)                     | Chamado quando o filtro interrompe o streaming. Virtual.                                                                                        |
| [**OnWaitEnd**](cbaserenderer-onwaitend.md)                                 | Chamado quando o filtro é feito aguardando o tempo de apresentação de um exemplo. Virtual.                                                       |
| [**OnWaitStart**](cbaserenderer-onwaitstart.md)                             | Chamado quando o filtro começa a aguardar o tempo de apresentação de um exemplo. Virtual.                                                        |
| [**PrepareRender**](cbaserenderer-preparerender.md)                         | Chamado antes de o filtro renderizar um exemplo. Virtual.                                                                                     |
| [**ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md)             | Determina como um exemplo é agendado para renderização. Virtual.                                                                            |
| Métodos virtuais puros                                                         | Descrição                                                                                                                             |
| [**Checkmediatype**](cbaserenderer-checkmediatype.md)                       | Determina se o filtro aceita um tipo de mídia específico.                                                                                 |
| [**DoRenderSample**](cbaserenderer-dorendersample.md)                       | Renderiza um exemplo.                                                                                                                       |
| Métodos IMediaFilter                                                         | Descrição                                                                                                                             |
| [**GetState**](cbaserenderer-getstate.md)                                   | Recupera o estado do filtro (em execução, parado ou em pausa).                                                                             |
| [**Pausar**](cbaserenderer-pause.md)                                         | Pausa o filtro.                                                                                                                      |
| [**Executar**](cbaserenderer-run.md)                                             | Executa o filtro.                                                                                                                        |
| [**Stop**](cbaserenderer-stop.md)                                           | Interrompe o filtro.                                                                                                                       |
| Métodos IBaseFilter                                                          | Descrição                                                                                                                             |
| [**Findpin**](cbaserenderer-findpin.md)                                     | Recupera o pino com o identificador especificado.                                                                                        |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parâmetro<br/>  | <dl> <dt>Renbase.h (incluir Fluxos.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (builds de varejo); </dt> <dt>Strmbasd.lib (builds de depuração)</dt> </dl> |



 

 




