---
description: Gerado por um sink de fluxo quando ele conclui a transição para o estado em pausa.
ms.assetid: 84ab62fc-1525-433c-8af5-70659122703c
title: Evento MEStreamSinkPaused (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bd3e278c4aeb72300af5ef3821a465ac493efa554ed86d798716ff6dffbf1ed
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119228596"
---
# <a name="mestreamsinkpaused-event"></a>Evento MEStreamSinkPaused

Gerado por um sink de fluxo quando ele conclui a transição para o estado em pausa. A transição para pausa ocorre quando o método [**IMFPresentationClock::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-pause) é chamado no relógio de apresentação do sink.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Sinks de mídia](media-sinks.md)
</dt> </dl>

 

 




