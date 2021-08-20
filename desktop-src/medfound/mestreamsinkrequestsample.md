---
description: Gerado por um coletor de fluxo para solicitar um novo exemplo de mídia do pipeline.
ms.assetid: 35020a15-942f-4dd0-9ca4-815affdacecf
title: Evento MEStreamSinkRequestSample (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de147486f54485ecb9f80b15394b1a2d48021c1f602ccd138cf6718ef7ec2c0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061321"
---
# <a name="mestreamsinkrequestsample-event"></a>Evento MEStreamSinkRequestSample

Gerado por um coletor de fluxo para solicitar um novo exemplo de mídia do pipeline. Para cada evento MEStreamSinkRequestSample, o pipeline solicita dados do próximo componente upstream.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



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

[Coletores de mídia](media-sinks.md)
</dt> </dl>

 

 




