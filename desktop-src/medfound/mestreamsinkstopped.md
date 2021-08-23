---
description: Gerado por um sink de fluxo quando ele conclui a transição para o estado parado. A transição para parado ocorre quando o método Stop IMFPresentationClock é chamado no relógio de apresentação dos sinks.
ms.assetid: 1a8c7faa-4d4a-4458-ad08-a760a15dc347
title: Evento MEStreamSinkStopped (Mfobjects.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7bf6a39dca8f50fed8fdd1d0137405225624999fab42771e485174ba4f0afa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715096"
---
# <a name="mestreamsinkstopped-event"></a>Evento MEStreamSinkStopped

Gerado por um sink de fluxo quando ele conclui a transição para o estado parado. A transição para parado ocorre quando o [**método IMFPresentationClock::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-stop) é chamado no relógio de apresentação do sink.

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
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Sinks de mídia](media-sinks.md)
</dt> </dl>

 

 




