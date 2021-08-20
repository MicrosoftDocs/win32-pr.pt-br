---
description: Gerado por um sink de fluxo quando ele conclui a transição para o estado de execução.
ms.assetid: 95ac658b-bec0-442d-85ef-61966b40a2f2
title: Evento MEStreamSinkStarted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b19d21559b8af53df47b2105f8c72b87a62b0439d1774257c044409554eaa19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118061230"
---
# <a name="mestreamsinkstarted-event"></a>Evento MEStreamSinkStarted

Gerado por um sink de fluxo quando ele conclui a transição para o estado de execução. A transição para a execução ocorre quando o [**método IMFPresentationClock::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-start) é chamado no relógio de apresentação do sink. O sink de mídia recebe a notificação por meio de [**seu método IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) ou [**IMFClockStateSink::OnClockRestart.**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockrestart)

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

 

 




