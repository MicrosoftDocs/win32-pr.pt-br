---
description: Códigos de notificação de eventos
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Códigos de notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9c41abc3ffc7a93a39e7a97fb210b491ad4fc58
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105792555"
---
# <a name="event-notification-codes"></a>Códigos de notificação de eventos

Esta seção lista os eventos do DirectShow que não são específicos do DVD. Para eventos específicos do DVD, consulte [códigos de notificação de eventos de DVD](dvd-notification-codes.md).

Os filtros enviam eventos para o Gerenciador do grafo de filtro chamando o método [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) . O Gerenciador de gráfico de filtro lida com alguns eventos e enfileira outras pessoas para o aplicativo. O aplicativo os recupera chamando o método [**IMediaEvent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) .

Nas seções a seguir, cada entrada lista o código do evento, o significado dos parâmetros do evento e a ação padrão do Gerenciador do grafo de filtro para o evento, se houver. Para substituir a ação padrão, chame [**IMediaEvent:: CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). Os códigos de evento são definidos nos arquivos de cabeçalho Evcode. h e Audevcod. h. Se não houver nenhuma ação padrão, o Gerenciador do grafo de filtro encaminhará automaticamente o evento para o aplicativo (por meio da fila de eventos).

**Eventos personalizados**

Os filtros podem definir eventos personalizados com códigos de eventos no intervalo do usuário do EC \_ e superior. O Gerenciador de gráficos de filtro os colocará diretamente na fila de eventos. No entanto, as seguintes advertências se aplicam:

-   O Gerenciador do grafo de filtro não pode liberar os parâmetros de evento usando o método normal [**IMediaEvent:: FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) . O aplicativo deve liberar qualquer quantidade de memória ou referência associada aos parâmetros do evento.
-   O filtro só deve enviar o evento de dentro de um aplicativo que esteja preparado para manipular o evento. (Possivelmente o aplicativo pode definir uma propriedade personalizada no filtro para indicar que é seguro enviar o evento.)



| Código de notificação de eventos                                                 | Descrição                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**ativação do EC \_**](ec-activate.md)                                     | Uma janela de vídeo está sendo ativada ou desativada.                                                                         |
| [**BANDWIDTHCHANGE do EC \_**](ec-bandwidthchange.md)                       | Não há suporte.                                                                                                            |
| [**dados de buffer do EC \_ \_**](ec-buffering-data.md)                        | O grafo está armazenando dados em buffer ou parou de armazenar em buffer os dados.                                                               |
| [**desenvolvido por EC \_**](ec-built.md)                                           | Envie pelo controle de vídeo quando um grafo tiver sido compilado. Não encaminhado para aplicativos.                                     |
| [**relógio do EC \_ \_ alterado**](ec-clock-changed.md)                          | O relógio de referência foi alterado.                                                                                          |
| [**desdefinição do relógio do EC \_ \_**](ec-clock-unset.md)                              | O provedor de relógio foi desconectado.                                                                                      |
| [**\_evento de CODECAPI do EC \_**](ec-codecapi-event.md)                        | Enviado por um codificador para sinalizar um evento de codificação.                                                                           |
| [**EC \_ concluído**](ec-complete.md)                                     | Todos os dados de um fluxo específico foram renderizados.                                                                      |
| [**o EC \_ ContentProperty \_ foi alterado**](ec-contentproperty-changed.md)      | Não há suporte.                                                                                                            |
| [**\_dispositivo EC \_ perdido**](ec-device-lost.md)                              | Um dispositivo Plug and Play foi removido ou ficou disponível novamente.                                                         |
| [**exibição do EC \_ \_ alterada**](ec-display-changed.md)                      | O modo de exibição foi alterado.                                                                                             |
| [**\_fim \_ do \_ segmento do EC**](ec-end-of-segment.md)                       | O fim de um segmento foi atingido.                                                                                    |
| [**EC \_ EOS em \_ breve**](ec-eos-soon.md)                                    | Não há suporte.                                                                                                            |
| [**\_STILLPLAYING de erro do EC \_**](ec-error-stillplaying.md)                | Falha em um comando assíncrono para executar o grafo.                                                                      |
| [**ERRORABORT do EC \_**](ec-errorabort.md)                                 | Uma operação foi anulada devido a um erro.                                                                             |
| [**ERRORABORTEX do EC \_**](ec-errorabortex.md)                             | Uma operação foi anulada devido a um erro.                                                                             |
| [**\_alteração do \_ modo de EXTDEVICE do EC \_**](ec-extdevice-mode-change.md)         | Não há suporte.                                                                                                            |
| [**\_arquivo EC \_ fechado**](ec-file-closed.md)                              | O arquivo de origem foi fechado devido a um evento inesperado.                                                                |
| [**\_tela inteira do EC \_ perdida**](ec-fullscreen-lost.md)                      | O processador de vídeo está alternando para o modo de tela inteira.                                                                  |
| [**gráfico do EC \_ \_ alterado**](ec-graph-changed.md)                          | O gráfico de filtro foi alterado.                                                                                             |
| [**tamanho do EC \_ \_ alterado**](ec-length-changed.md)                        | O comprimento de uma fonte foi alterado.                                                                                       |
| [**loadstatus do EC \_**](ec-loadstatus.md)                                 | Notifica o aplicativo sobre o progresso ao abrir um arquivo de rede.                                                         |
| [**\_ocorrência do marcador do EC \_**](ec-marker-hit.md)                                | Não há suporte.                                                                                                            |
| [**o EC \_ precisa ser \_ reiniciado**](ec-need-restart.md)                            | Um filtro está solicitando que o grafo seja reiniciado.                                                                       |
| [**\_novo \_ PIN do EC**](ec-new-pin.md)                                      | Não há suporte.                                                                                                            |
| [**\_janela de notificação do EC \_**](ec-notify-window.md)                          | Notifica um filtro sobre a janela do processador de vídeo.                                                                         |
| [**\_evento OLE do EC \_**](ec-ole-event.md)                                  | Um filtro está passando uma cadeia de texto para o aplicativo.                                                                     |
| [**\_arquivo de abertura do EC \_**](ec-opening-file.md)                            | O grafo está abrindo um arquivo ou terminou de abrir um arquivo.                                                              |
| [**paleta do EC \_ \_ alterada**](ec-palette-changed.md)                      | A paleta de vídeos foi alterada.                                                                                            |
| [**EC em \_ pausa**](ec-paused.md)                                         | Uma solicitação de pausa foi concluída.                                                                                            |
| [**EC \_ , \_ reabra**](ec-please-reopen.md)                          | O arquivo de origem foi alterado.                                                                                              |
| [**pré-processamento de EC \_ \_ concluído**](ec-preprocess-complete.md)              | Enviado pelo filtro do [gravador ASF do WM](wm-asf-writer-filter.md) quando ele conclui o pré-processamento para codificação de passagem. |
| [**\_latência de processamento do EC \_**](ec-processing-latency.md)                | Indica a quantidade de tempo que um componente está demorando para processar cada exemplo.                                           |
| [**\_alteração de qualidade do EC \_**](ec-quality-change.md)                        | O grafo está descartando amostras, para controle de qualidade.                                                                       |
| [**renderização de EC \_ \_ concluída**](ec-render-finished.md)                      | Não há suporte.                                                                                                            |
| [**redesenho de EC \_**](ec-repaint.md)                                       | Um processador de vídeo requer um redesenho.                                                                                      |
| [**\_latência de exemplo de EC \_**](ec-sample-latency.md)                        | Especifica o quanto o agendamento de um componente é muito atrasado para o processamento de exemplos.                                                  |
| [**exemplo de EC \_ \_ necessário**](ec-sample-needed.md)                          | Solicita uma nova amostra de entrada do filtro EVR (processador de vídeo avançado).                                                |
| [**\_hora de limpeza do EC \_**](ec-scrub-time.md)                                | Especifica o carimbo de data/hora para a etapa de quadro mais recente.                                                                  |
| [**segmento de EC \_ \_ iniciado**](ec-segment-started.md)                      | Um novo segmento foi iniciado.                                                                                                |
| [**desligar \_ o EC \_**](ec-shutting-down.md)                          | O grafo de filtro está sendo desligado, antes de ser destruído.                                                              |
| [**\_SNDDEV \_ de EC em \_ erro**](ec-snddev-in-error.md)                     | Ocorreu um erro de dispositivo em um filtro de captura de áudio.                                                                   |
| [**erro do EC \_ SNDDEV \_ out \_**](ec-snddev-out-error.md)                   | Ocorreu um erro de dispositivo em um filtro de processador de áudio.                                                                  |
| [**\_privação de EC**](ec-starvation.md)                                 | Um filtro não está recebendo dados suficientes.                                                                                    |
| [**\_alteração de estado do EC \_**](ec-state-change.md)                            | O estado do grafo de filtro foi alterado.                                                                                       |
| [**STATUS do EC \_**](ec-status.md)                                         | Contém duas cadeias de caracteres de status arbitrárias.                                                                                    |
| [**etapa do EC \_ \_ concluída**](ec-step-complete.md)                          | Um filtro que executa a revisão do quadro excedeu o número especificado de quadros.                                            |
| [**controle de fluxo de EC \_ \_ \_ iniciado**](ec-stream-control-started.md)       | Um comando de início de controle de fluxo entrou em vigor.                                                                          |
| [**controle de fluxo do EC \_ \_ \_ interrompido**](ec-stream-control-stopped.md)       | Um comando de parada de controle de fluxo teve efeito.                                                                           |
| [**\_STILLPLAYING de \_ erro de fluxo do EC \_**](ec-stream-error-stillplaying.md) | Ocorreu um erro em um fluxo. O fluxo ainda está em execução.                                                           |
| [**erro de fluxo de EC \_ \_ \_ interrompido**](ec-stream-error-stopped.md)           | Um fluxo foi interrompido devido a um erro.                                                                                 |
| [**código de meio do EC \_ \_ disponível**](ec-timecode-available.md)                | Não há suporte.                                                                                                            |
| [**EC não \_ compilado**](ec-unbuilt.md)                                       | Envie pelo controle de vídeo quando um grafo tiver sido interrompido. Não encaminhado para aplicativos.                                 |
| [**autoanulação do EC \_**](ec-userabort.md)                                   | O usuário terminou a reprodução.                                                                                         |
| [**tamanho de vídeo do EC \_ \_ \_ alterado**](ec-video-size-changed.md)               | O tamanho do vídeo nativo foi alterado.                                                                                        |
| [**VIDEOFRAMEREADY do EC \_**](ec-videoframeready.md)                       | Um quadro de vídeo está pronto para exibição.                                                                                       |
| [**\_ \_ falha na reconexão do EC VMR \_**](ec-vmr-reconnection-failed.md)     | Enviado pelo VMR-7 e o VMR-9 quando não foi possível aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.   |
| [**conjunto de RENDERDEVICE do EC \_ VMR \_ \_**](ec-vmr-renderdevice-set.md)           | Enviado quando o VMR seleciona seu mecanismo de renderização.                                                                   |
| [**superfície do EC \_ VMR \_ \_ invertida**](ec-vmr-surface-flipped.md)             | Enviado quando o apresentador de alocador VMR-7's chamou o método flip do DirectDraw na superfície apresentada.           |
| [**janela do EC \_ \_ destruída**](ec-window-destroyed.md)                    | O processador de vídeo foi destruído ou removido do grafo.                                                               |
| [**\_evento de WMT do EC \_**](ec-wmt-event.md)                                  | Enviado pelo filtro de leitor ASF do WM quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).                    |
| [**evento de índice do EC \_ WMT \_ \_**](ec-wmt-index-event.md)                     | Enviado quando um aplicativo usa o gravador ASF do WM para indexar arquivos de vídeo do Windows Media.                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Notificação de eventos no DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



