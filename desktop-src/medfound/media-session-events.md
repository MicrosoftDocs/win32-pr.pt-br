---
description: Eventos de sessão de mídia
ms.assetid: 882a01f2-8f5c-4640-a8ac-f4f5860d7ed1
title: Eventos de sessão de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffecb3f4e3f4b3a3b30be95fcc45adcb81c1a84dd04ed8cf637bad759512a06
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119724006"
---
# <a name="media-session-events"></a>Eventos de sessão de mídia

A maioria das operações da sessão de mídia é executada de forma assíncrona, portanto, o aplicativo deve escutar eventos usando a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) da sessão de mídia. (A interface [**IMFMediaSession**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession) herda **IMFMediaEventGenerator**.) A sequência exata de eventos dependerá do seu aplicativo, mas os eventos a seguir são gerados pela sessão de mídia em quase todas as situações.



| Evento                                                                  | Descrição                                                                                                                                                                                                                    |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MEEndOfPresentation](meendofpresentation.md)                         | Gerado quando a origem da mídia tiver concluído a apresentação. Os dados ainda podem estar passando pelo pipeline no momento.                                                                                                     |
| [MEError](meerror.md)                                                 | Gerado se ocorrer um erro durante o streaming.                                                                                                                                                                                    |
| [MESessionClosed](mesessionclosed.md)                                 | Gerado quando o método [**Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) é concluído. Esse evento é o último evento que a sessão de mídia enfileira. Depois de receber esse evento, é seguro desligar todas as fontes de mídia que você criou. |
| [MESessionEnded](mesessionended.md)                                   | Gerado quando a sessão de mídia é concluída com a última apresentação.                                                                                                                                                              |
| [MESessionNotifyPresentationTime](mesessionnotifypresentationtime.md) | Notifica a aplicação da hora da apresentação quando a nova apresentação será iniciada.                                                                                                                                        |
| [MESessionStarted](mesessionstarted.md)                               | Gerado quando o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) é concluído. A menos que tenha ocorrido um erro, os dados estão se movendo pelo pipeline neste ponto.                                                                          |
| [MESessionTopologySet](mesessiontopologyset.md)                       | Gerado quando o método [**settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) é concluído. A menos que ocorra um erro, o aplicativo não precisa realizar nenhuma ação.                                                                 |
| [MESessionTopologyStatus](mesessiontopologystatus.md)                 | Gerado em várias vezes quando o status de uma topologia é alterado.                                                                                                                                                                 |



 

O método [**IMFMediaSession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) não gera um evento. O método de **desligamento** é síncrono. Após esse método retornar, é seguro liberar o ponteiro de retorno de chamada do evento.

Além dos eventos da sessão de mídia, o aplicativo pode receber eventos dos coletores de mídia na topologia. Eles podem ser eventos personalizados definidos pelo coletor de mídia, que podem conter dados arbitrários. Por exemplo, o coletor pode derivar os dados de evento dos dados de origem, que podem ser de uma fonte externa não confiável. Um aplicativo deve ignorar todos os eventos não reconhecidos e ter cuidado ao analisar dados de eventos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sessão de mídia](media-session.md)
</dt> </dl>

 

 



