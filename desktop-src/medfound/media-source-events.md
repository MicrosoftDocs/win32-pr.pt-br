---
description: Eventos de origem de mídia
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventos de origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105791589"
---
# <a name="media-source-events"></a>Eventos de origem de mídia

Este tópico lista os eventos que são enviados por fontes de mídia e fluxos de mídia. As fontes de mídia também podem enviar eventos personalizados não listados aqui.

## <a name="media-source-events"></a>Eventos de origem de mídia



| Evento                                                                      | Descrição                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [Evento MEEndOfPresentation](meendofpresentation.md)                       | A apresentação terminou. Todos os fluxos na apresentação atingiram o final do fluxo.      |
| [Evento MENewStream](menewstream.md)                                       | Um novo fluxo foi criado. O evento contém um ponteiro para o fluxo.                            |
| [Evento MESourceCharacteristicsChanged](mesourcecharacteristicschanged.md) | As características da fonte foram alteradas. (Opcional).                                      |
| [Evento MESourceMetadataChanged](mesourcemetadatachanged.md)               | Os metadados da origem foram alterados. (Opcional).                                                   |
| [Evento MESourcePaused](mesourcepaused.md)                                 | A origem foi pausada. Nem todas as fontes dão suporte à pausa.                                          |
| [Evento MESourceRateChanged](mesourceratechanged.md)                       | A taxa de reprodução da origem foi alterada. (Opcional; aplica-se se a fonte der suporte ao controle de taxa.) |
| [Evento MESourceRateChangeRequested](mesourceratechangerequested.md)       | A origem está solicitando uma nova taxa de reprodução. (Opcional).                                        |
| [Evento MESourceSeeked](mesourceseeked.md)                                 | A origem foi procurada. Nem todas as fontes dão suporte à busca.                                          |
| [Evento MESourceStarted](mesourcestarted.md)                               | A origem foi iniciada.                                                                          |
| [Evento MESourceStopped](mesourcestopped.md)                               | A origem foi parada.                                                                          |
| [Evento MEUpdatedStream](meupdatedstream.md)                               | Um fluxo existente foi buscado ou reiniciado. O evento contém um ponteiro para o fluxo.         |



 

## <a name="media-stream-events"></a>Eventos de fluxo de mídia



| Evento                                                    | Descrição                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [Evento MEEndOfStream](meendofstream.md)                 | O fluxo terminou.                                                                                                              |
| [Evento MEError](meerror.md)                             | Ocorreu um erro durante o streaming. Use esse evento para erros que não estão relacionados a nenhum dos outros eventos listados aqui. |
| [Evento MEMediaSample](memediasample.md)                 | O fluxo gerou uma nova amostra.                                                                                         |
| [Evento MEStreamFormatChanged](mestreamformatchanged.md) | O tipo de mídia foi alterado. (Opcional).                                                                                        |
| [Evento MEStreamPaused](mestreampaused.md)               | O fluxo foi pausado.                                                                                                         |
| [Evento MEStreamSeeked](mestreamseeked.md)               | O fluxo foi buscado.                                                                                                         |
| [Evento MEStreamStarted](mestreamstarted.md)             | O fluxo foi iniciado.                                                                                                        |
| [Evento MEStreamStopped](mestreamstopped.md)             | O fluxo foi interrompido.                                                                                                        |
| [Evento MEStreamThinMode](mestreamthinmode.md)           | O modo de finamento foi iniciado ou interrompido. (Opcional).                                                                              |
| [Evento MEStreamTick](mestreamtick.md)                   | Há uma lacuna no fluxo. (Opcional).                                                                                      |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> </dl>

 

 



