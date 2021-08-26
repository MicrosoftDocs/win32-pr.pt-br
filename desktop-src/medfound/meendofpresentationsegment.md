---
description: Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento. Quando o segmento final é concluído, a origem do sequenciador gera um evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b82f646ca76dbb6cc3cd8dc9e95dbaca2c55c504af261924918dbf790411e7d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013696"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Sobre a origem do sequenciador](about-the-sequencer-source.md)
</dt> <dt>

[Eventos de origem do Sequencer](sequencer-source-events.md)
</dt> </dl>

 

 




