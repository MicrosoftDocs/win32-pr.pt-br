---
description: Atributos de evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b36d64efbc4ed36569ef85514d38563fe09a01902218833b029455c48e2c6e3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600506"
---
# <a name="event-attributes-microsoft-media-foundation"></a>Atributos de evento (Microsoft Media Foundation)

Os atributos a seguir se aplicam a eventos.



| Atributo                                                                                                        | Descrição                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**MF \_ EVENT \_ DO \_ THINNING**](mf-event-do-thinning-attribute.md)                                                | Quando uma fonte de mídia solicita uma nova taxa de reprodução, especifica se a origem também solicita a afinação.                |
| [**NÓ DE \_ SAÍDA DO \_ EVENTO \_ MF**](mf-event-output-node-attribute.md)                                                | Identifica o nó de topologia para um sink de fluxo.                                                                       |
| [**DESLOCAMENTO DE TEMPO \_ DE APRESENTAÇÃO DO EVENTO \_ \_ \_ MF**](mf-event-presentation-time-offset-attribute.md)                     | Deslocamento entre a hora da apresentação e os carimbos de data/hora da fonte de mídia.                                              |
| [**HORA DE \_ \_ LIMPEZA DO EVENTO MF \_**](mf-event-scrubsample-time-attribute.md)                                      | Tempo de apresentação para um exemplo que foi renderizado durante a depuração.                                                     |
| [**\_ \_ SESSIONCAPS DE EVENTO MF**](mf-event-sessioncaps-attribute.md)                                                 | Contém sinalizadores que definem os recursos da Sessão de Mídia, com base na apresentação atual.                  |
| [**DELTA \_ \_ SESSIONCAPS DO EVENTO MF \_**](mf-event-sessioncaps-delta-attribute.md)                                    | Contém sinalizadores que indicam quais recursos foram alterados na Sessão de Mídia, com base na apresentação atual. |
| [**INÍCIO REAL \_ DA \_ ORIGEM \_ DO EVENTO \_ MF**](mf-event-source-actual-start-attribute.md)                               | Contém a hora de início quando uma fonte de mídia é reiniciada de sua posição atual.                                       |
| [**CARACTERÍSTICAS DA \_ ORIGEM \_ DO EVENTO \_ MF**](mf-event-source-characteristics-attribute.md)                          | Especifica as características atuais da fonte de mídia.                                                            |
| [**CARACTERÍSTICAS ANTIGAS \_ DA \_ ORIGEM \_ DO \_ EVENTO MF**](mf-event-source-characteristics-old-attribute.md)                 | Especifica as características anteriores da fonte de mídia.                                                           |
| [**INÍCIO FALSO \_ DA \_ ORIGEM \_ DO EVENTO \_ MF**](mf-event-source-fake-start-attribute.md)                                   | Especifica se a topologia de segmento atual está vazia.                                                              |
| [**INÍCIO DO PROJETO \_ DE \_ ORIGEM \_ DO EVENTO MF**](mf-event-source-projectstart-attribute.md)                                | Especifica a hora de início de uma topologia de segmento.                                                                      |
| [**TOPOLOGIA DE \_ \_ ORIGEM DO \_ EVENTO MF \_ CANCELADA**](mf-event-source-topology-canceled-attribute.md)                     | Especifica se a origem do sequenciador cancelou uma topologia.                                                           |
| [**HORA DE INÍCIO \_ DA APRESENTAÇÃO DO EVENTO \_ \_ \_ MF**](mf-event-start-presentation-time-attribute.md)                       | A hora de início da apresentação, em unidades de 100 nanossegundos, conforme medido pelo relógio de apresentação.               |
| [**HORA DE INÍCIO DA APRESENTAÇÃO DO EVENTO MF \_ \_ NA \_ \_ \_ \_ SAÍDA**](mf-event-start-presentation-time-at-output-attribute.md) | A hora de apresentação em que os sinks de mídia renderizarão a primeira amostra da nova topologia.                      |
| [**STATUS DA \_ TOPOLOGIA DE \_ \_ EVENTO MF**](mf-event-topology-status-attribute.md)                                        | Especifica o status de uma topologia durante a reprodução.                                                                   |
| [**HORA DE OCORRÊNCIA \_ \_ DE EVENTO \_ APROXIMADO DA \_ \_ SESSÃO MF**](mf-session-approx-event-occurrence-time-attribute.md)        | O tempo aproximado em que a Sessão de Mídia gerou um evento.                                                          |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IMFMediaEvent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Media Foundation atributos](media-foundation-attributes.md)
</dt> </dl>

 

 



