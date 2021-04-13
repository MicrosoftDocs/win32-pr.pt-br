---
description: Atributos do evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501170"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Atributos de evento (Microsoft Media Foundation)

Os atributos a seguir se aplicam a eventos.



| Atributo                                                                                                        | Descrição                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**o \_ evento MF \_ faz a \_ finação**](mf-event-do-thinning-attribute.md)                                                | Quando uma fonte de mídia solicita uma nova taxa de reprodução, especifica se a origem também solicita a fina.                |
| [**\_nó de \_ saída do evento MF \_**](mf-event-output-node-attribute.md)                                                | Identifica o nó de topologia para um coletor de fluxo.                                                                       |
| [**\_deslocamento do \_ tempo de apresentação do evento MF \_ \_**](mf-event-presentation-time-offset-attribute.md)                     | Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.                                              |
| [**\_tempo de \_ SCRUBSAMPLE do evento MF \_**](mf-event-scrubsample-time-attribute.md)                                      | Tempo de apresentação para um exemplo que foi renderizado durante a depuração.                                                     |
| [**\_SESSIONCAPS do evento MF \_**](mf-event-sessioncaps-attribute.md)                                                 | Contém sinalizadores que definem os recursos da sessão de mídia, com base na apresentação atual.                  |
| [**\_ \_ SESSIONCAPS Delta de evento MF \_**](mf-event-sessioncaps-delta-attribute.md)                                    | Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual. |
| [**\_ \_ início real da origem do evento MF \_ \_**](mf-event-source-actual-start-attribute.md)                               | Contém a hora de início quando uma fonte de mídia é reiniciada a partir de sua posição atual.                                       |
| [**\_características de \_ origem do evento MF \_**](mf-event-source-characteristics-attribute.md)                          | Especifica as características atuais da origem da mídia.                                                            |
| [**\_características de origem do evento MF \_ \_ \_ antigas**](mf-event-source-characteristics-old-attribute.md)                 | Especifica as características anteriores da origem da mídia.                                                           |
| [**\_ \_ Início falso da origem do evento MF \_ \_**](mf-event-source-fake-start-attribute.md)                                   | Especifica se a topologia de segmento atual está vazia.                                                              |
| [**\_origem do evento MF \_ \_ PROJECTSTART**](mf-event-source-projectstart-attribute.md)                                | Especifica a hora de início para uma topologia de segmento.                                                                      |
| [**\_topologia de origem do evento MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)                     | Especifica se a origem do sequenciador cancelou uma topologia.                                                           |
| [**\_hora de \_ início da \_ apresentação \_ do evento MF**](mf-event-start-presentation-time-attribute.md)                       | A hora de início da apresentação, em unidades de 100 nanossegundos, conforme medida pelo relógio de apresentação.               |
| [**\_ \_ \_ hora de início da apresentação do evento MF \_ \_ na \_ saída**](mf-event-start-presentation-time-at-output-attribute.md) | A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.                      |
| [**\_status da \_ topologia de evento MF \_**](mf-event-topology-status-attribute.md)                                        | Especifica o status de uma topologia durante a reprodução.                                                                   |
| [**\_tempo de \_ \_ ocorrência de evento aprox da sessão \_ MF \_**](mf-session-approx-event-occurrence-time-attribute.md)        | A hora aproximada em que a sessão de mídia gerou um evento.                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



