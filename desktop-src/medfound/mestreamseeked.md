---
description: 'Gerado por um fluxo de mídia após uma chamada para IMFMediaSource:: Start causa uma busca no fluxo. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento MESourceSeeked.'
ms.assetid: df06df16-711d-4262-b049-fb29f25934de
title: Evento MEStreamSeeked (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7b66e2176b08c04b01fc487aac4b8218536b615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165036"
---
# <a name="mestreamseeked-event"></a>Evento MEStreamSeeked

Gerado por um fluxo de mídia após uma chamada para [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) causa uma busca no fluxo. Um fluxo de mídia gera esse evento quando a origem da mídia gera o evento [MESourceSeeked](mesourceseeked.md) .

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                                                        |
|-------------------|--------------------------------------------------------------------|
| VT \_ i8<br/> | Nova hora de início, em unidades de 100 a nanossegundos.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




