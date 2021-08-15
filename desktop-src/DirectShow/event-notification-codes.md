---
description: Códigos de notificação de eventos
ms.assetid: 339ffcd9-7724-4c92-b241-afbed81d9380
title: Códigos de notificação de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54792e433535ceefad416033d7758f4398b7777951173256c9be9b83913d61f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015784"
---
# <a name="event-notification-codes"></a>Códigos de notificação de eventos

Esta seção lista os DirectShow eventos que não são específicos do DVD. Para eventos específicos ao DVD, consulte [Códigos de notificação de evento de DVD](dvd-notification-codes.md).

Os filtros enviam eventos para o Gerenciador Graph Filtro chamando o [**método IMediaEventSink::Notify.**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) O Gerenciador Graph Filtro lida com alguns eventos e enfiltre outros para o aplicativo. O aplicativo os recupera chamando o [**método IMediaEvent::GetEvent.**](/windows/desktop/api/Control/nf-control-imediaevent-getevent)

Nas seções a seguir, cada entrada lista o código do evento, o significado dos parâmetros de evento e a ação padrão do Gerenciador Graph Filtro para o evento, se for o caso. Para substituir a ação padrão, chame [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling). Os códigos de evento são definidos nos arquivos de header Evcode.h e Audevcod.h. Se não houver nenhuma ação padrão, o Gerenciador Graph Filtrar encaminhará automaticamente o evento para o aplicativo (por meio da fila de eventos).

**Eventos personalizados**

Os filtros podem definir eventos personalizados com códigos de evento no intervalo EC \_ USER e superior. O Gerenciador Graph Filtro os colocará diretamente na fila de eventos. No entanto, as seguintes advertências se aplicam:

-   O Gerenciador Graph Filtro não pode liberar os parâmetros de evento usando o método [**normal IMediaEvent::FreeEventParams.**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) O aplicativo deve liberar todas as contagens de memória ou referência associadas aos parâmetros de evento.
-   O filtro só deve enviar o evento de dentro de um aplicativo que esteja preparado para manipular o evento. (Possivelmente, o aplicativo pode definir uma propriedade personalizada no filtro para indicar que é seguro enviar o evento.)



| Código de notificação de eventos                                                 | Descrição                                                                                                               |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**EC \_ ACTIVATE**](ec-activate.md)                                     | Uma janela de vídeo está sendo ativada ou desativada.                                                                         |
| [**EC \_ BANDWIDTHCHANGE**](ec-bandwidthchange.md)                       | Sem suporte.                                                                                                            |
| [**DADOS \_ DE BUFFER DE \_ EC**](ec-buffering-data.md)                        | O grafo está em buffer de dados ou parou de colocar dados em buffer.                                                               |
| [**EC \_ BUILT**](ec-built.md)                                           | Enviar pelo Controle de Vídeo quando um grafo tiver sido criado. Não encaminhado para aplicativos.                                     |
| [**RELÓGIO \_ DE EC \_ ALTERADO**](ec-clock-changed.md)                          | O relógio de referência foi alterado.                                                                                          |
| [**EC \_ CLOCK \_ UNSET**](ec-clock-unset.md)                              | O provedor de relógio foi desconectado.                                                                                      |
| [**EVENTO \_ EC CODECAPI \_**](ec-codecapi-event.md)                        | Enviado por um codificador para sinalizar um evento de codificação.                                                                           |
| [**EC \_ COMPLETE**](ec-complete.md)                                     | Todos os dados de um fluxo específico foram renderizados.                                                                      |
| [**EC \_ CONTENTPROPERTY \_ ALTERADO**](ec-contentproperty-changed.md)      | Sem suporte.                                                                                                            |
| [**DISPOSITIVO \_ EC \_ PERDIDO**](ec-device-lost.md)                              | Um Plug and Play foi removido ou se tornou disponível novamente.                                                         |
| [**EXIBIÇÃO DE EC \_ \_ ALTERADA**](ec-display-changed.md)                      | O modo de exibição foi alterado.                                                                                             |
| [**EC \_ END \_ OF \_ SEGMENT**](ec-end-of-segment.md)                       | O final de um segmento foi atingido.                                                                                    |
| [**EC \_ EOS \_ EM BREVE**](ec-eos-soon.md)                                    | Sem suporte.                                                                                                            |
| [**ERRO \_ DE EC \_ STILLPLAYING**](ec-error-stillplaying.md)                | Um comando assíncrono para executar o grafo falhou.                                                                      |
| [**EC \_ ERRORABORT**](ec-errorabort.md)                                 | Uma operação foi anulada devido a um erro.                                                                             |
| [**EC \_ ERRORABORTEX**](ec-errorabortex.md)                             | Uma operação foi anulada devido a um erro.                                                                             |
| [**EC \_ EXTDEVICE \_ MODE \_ CHANGE**](ec-extdevice-mode-change.md)         | Sem suporte.                                                                                                            |
| [**ARQUIVO \_ DE EC \_ FECHADO**](ec-file-closed.md)                              | O arquivo de origem foi fechado devido a um evento inesperado.                                                                |
| [**EC \_ FULLSCREEN \_ LOST**](ec-fullscreen-lost.md)                      | O renderador de vídeo está saindo do modo de tela inteira.                                                                  |
| [**GRAFO DE EC \_ \_ ALTERADO**](ec-graph-changed.md)                          | O grafo de filtro foi alterado.                                                                                             |
| [**COMPRIMENTO DA EC \_ \_ ALTERADO**](ec-length-changed.md)                        | O comprimento de uma origem foi alterado.                                                                                       |
| [**EC \_ LOADSTATUS**](ec-loadstatus.md)                                 | Notifica o aplicativo de progresso ao abrir um arquivo de rede.                                                         |
| [**EC \_ MARKER \_ HIT**](ec-marker-hit.md)                                | Sem suporte.                                                                                                            |
| [**EC \_ NEED \_ RESTART**](ec-need-restart.md)                            | Um filtro está solicitando que o grafo seja reiniciado.                                                                       |
| [**NOVO \_ PIN DE \_ EC**](ec-new-pin.md)                                      | Sem suporte.                                                                                                            |
| [**JANELA \_ NOTIFICAÇÃO \_ DE EC**](ec-notify-window.md)                          | Notifica um filtro da janela do renderador de vídeo.                                                                         |
| [**EVENTO \_ EC OLE \_**](ec-ole-event.md)                                  | Um filtro está passando uma cadeia de caracteres de texto para o aplicativo.                                                                     |
| [**ARQUIVO DE \_ ABERTURA \_ DE EC**](ec-opening-file.md)                            | O grafo está abrindo um arquivo ou concluiu a abertura de um arquivo.                                                              |
| [**PALETA \_ DE EC \_ ALTERADA**](ec-palette-changed.md)                      | A paleta de vídeos foi alterada.                                                                                            |
| [**EC \_ PAUSED**](ec-paused.md)                                         | Uma solicitação de pausa foi concluída.                                                                                            |
| [**EC \_ \_ REABRIR**](ec-please-reopen.md)                          | O arquivo de origem foi alterado.                                                                                              |
| [**\_PRÉ-PROCESSAMENTO DE \_ EC CONCLUÍDO**](ec-preprocess-complete.md)              | Enviado pelo [filtro Wm ASF Writer](wm-asf-writer-filter.md) quando ele conclui o pré-processamento para codificação multipasso. |
| [**LATÊNCIA \_ DE \_ PROCESSAMENTO DE EC**](ec-processing-latency.md)                | Indica a quantidade de tempo que um componente está levando para processar cada amostra.                                           |
| [**ALTERAÇÃO \_ DE QUALIDADE DA \_ EC**](ec-quality-change.md)                        | O grafo está soltando amostras para controle de qualidade.                                                                       |
| [**EC \_ RENDER \_ FINISHED**](ec-render-finished.md)                      | Sem suporte.                                                                                                            |
| [**EC \_ REPAINT**](ec-repaint.md)                                       | Um renderador de vídeo requer uma reint.                                                                                      |
| [**LATÊNCIA \_ DE \_ EXEMPLO DE EC**](ec-sample-latency.md)                        | Especifica o quão atrasado o agendamento de um componente está para processar exemplos.                                                  |
| [**EXEMPLO \_ DE EC \_ NECESSÁRIO**](ec-sample-needed.md)                          | Solicita um novo exemplo de entrada do filtro EVR (Renderização de Vídeo Aprimorado).                                                |
| [**TEMPO \_ DE LIMPEZA DE \_ EC**](ec-scrub-time.md)                                | Especifica o carimbo de data/hora da etapa de quadro mais recente.                                                                  |
| [**SEGMENTO \_ DE EC \_ INICIADO**](ec-segment-started.md)                      | Um novo segmento foi iniciado.                                                                                                |
| [**DESLIGAMENTO \_ DA \_ EC**](ec-shutting-down.md)                          | O grafo de filtro está sendo desligado, antes de ser destruído.                                                              |
| [**EC \_ SNDDEV \_ EM \_ ERRO**](ec-snddev-in-error.md)                     | Ocorreu um erro de dispositivo em um filtro de captura de áudio.                                                                   |
| [**ERRO \_ EC SNDDEV \_ \_ OUT**](ec-snddev-out-error.md)                   | Ocorreu um erro de dispositivo em um filtro do renderador de áudio.                                                                  |
| [**EC \_ STARVATION**](ec-starvation.md)                                 | Um filtro não está recebendo dados suficientes.                                                                                    |
| [**ALTERAÇÃO \_ DE ESTADO DA \_ EC**](ec-state-change.md)                            | O grafo de filtro alterou o estado.                                                                                       |
| [**STATUS DA \_ EC**](ec-status.md)                                         | Contém duas cadeias de caracteres de status arbitrárias.                                                                                    |
| [**ETAPA \_ EC \_ CONCLUÍDA**](ec-step-complete.md)                          | Um filtro executando a execução da execução de uma execução de quadro pisou o número especificado de quadros.                                            |
| [**CONTROLE DE FLUXO DE EC \_ \_ \_ INICIADO**](ec-stream-control-started.md)       | Um comando de início de controle de fluxo teve efeito.                                                                          |
| [**CONTROLE DE FLUXO DE EC \_ \_ \_ INTERROMPIDO**](ec-stream-control-stopped.md)       | Um comando stream-control stop teve efeito.                                                                           |
| [**ERRO \_ DE FLUXO DE EC AINDA EM \_ \_ REPRODUÇÃO**](ec-stream-error-stillplaying.md) | Ocorreu um erro em um fluxo. O fluxo ainda está em reprodução.                                                           |
| [**ERRO DE \_ FLUXO \_ DE EC \_ PARADO**](ec-stream-error-stopped.md)           | Um fluxo foi interrompido devido a um erro.                                                                                 |
| [**EC \_ TIMECODE \_ DISPONÍVEL**](ec-timecode-available.md)                | Sem suporte.                                                                                                            |
| [**EC \_ UNBUILT**](ec-unbuilt.md)                                       | Envie pelo Controle de Vídeo quando um grafo tiver sido dividido. Não encaminhado para aplicativos.                                 |
| [**EC \_ USERABORT**](ec-userabort.md)                                   | O usuário terminou a reprodução.                                                                                         |
| [**TAMANHO DO VÍDEO DE EC \_ \_ \_ ALTERADO**](ec-video-size-changed.md)               | O tamanho do vídeo nativo foi alterado.                                                                                        |
| [**EC \_ VIDEOFRAMEREADY**](ec-videoframeready.md)                       | Um quadro de vídeo está pronto para exibição.                                                                                       |
| [**FALHA NA RECONEXÃO DA \_ VMR \_ \_ DE EC**](ec-vmr-reconnection-failed.md)     | Enviado pela VMR-7 e pela VMR-9 quando não pôde aceitar uma solicitação de alteração de formato dinâmico do decodificador upstream.   |
| [**EC \_ VMR \_ RENDERDEVICE \_ SET**](ec-vmr-renderdevice-set.md)           | Enviado quando a VMR selecionou seu mecanismo de renderização.                                                                   |
| [**SUPERFÍCIE \_ DE VMR DE EC \_ \_ INVERTIDA**](ec-vmr-surface-flipped.md)             | Enviado quando o apresentador de alocador da VMR-7 chamou o método Flip do DirectDraw na superfície que está sendo apresentada.           |
| [**JANELA \_ EC \_ DESTRUÍDA**](ec-window-destroyed.md)                    | O renderador de vídeo foi destruído ou removido do grafo.                                                               |
| [**EVENTO \_ EC WMT \_**](ec-wmt-event.md)                                  | Enviado pelo filtro Leitor do WM ASF quando ele lê arquivos ASF protegidos pelo DRM (gerenciamento de direitos digitais).                    |
| [**EVENTO EC \_ WMT \_ INDEX \_**](ec-wmt-index-event.md)                     | Enviado quando um aplicativo usa o Wm ASF Writer para indexar Windows de Vídeo de Mídia.                                       |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> <dt>

[Notificação de eventos DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



