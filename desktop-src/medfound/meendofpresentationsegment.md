---
description: Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento. Quando o segmento final é concluído, a origem do sequenciador gera um evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827640"
---
# <a name="meendofpresentationsegment-event"></a>Evento MEEndOfPresentationSegment

Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento. Quando o segmento final é concluído, a origem do sequenciador gera um evento [MEEndOfPresentation](meendofpresentation.md) .

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                                               | Descrição                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**\_topologia de origem do evento MF \_ \_ \_ cancelada**](mf-event-source-topology-canceled-attribute.md)<br/> | Especifica se a origem do sequenciador cancelou esse segmento.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Sobre a origem do sequenciador](about-the-sequencer-source.md)
</dt> <dt>

[Eventos de origem do Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




