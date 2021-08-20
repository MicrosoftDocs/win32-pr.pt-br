---
description: Sinaliza um evento de um coletor de mídia que renderiza dados de mídia.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9fc70505033b9d88cd9593d2efa9f3c591f69f5e25bd968b06686c4c6ac911d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061851"
---
# <a name="merendererevent-event"></a>Evento MERendererEvent

Sinaliza um evento de um coletor de mídia que renderiza dados de mídia.

O [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) envia esse evento quando recebe um evento de usuário do apresentador EVR.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                        |
|-------------------|------------------------------------|
| \_I4 VT<br/> | Código do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Se o apresentador chama o método **IMediaEventSink:: Notify** do EVR com um código de evento no intervalo do usuário do EC \_ ou superior, o EVR envia esse evento. Os dados do evento são o código do evento que foi passado para o método **Notify** .

Os parâmetros de evento original (*EventParam1* e *EventParam2* no método **IMediaEventSink:: Notify** ) são ignorados, portanto, o apresentador deve definir esses valores como **NULL**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




