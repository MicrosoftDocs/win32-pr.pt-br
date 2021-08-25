---
description: Gerado por um sink de fluxo quando a taxa foi alterada.
ms.assetid: c61c71de-fd3c-429b-a29f-f9d2bbfcb531
title: Evento MEStreamSinkRateChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43a3a4cbff4464f78e71d3047e2b9ccaddfcbf38adcb5e84bab8f5ae49c5d80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827136"
---
# <a name="mestreamsinkratechanged-event"></a>Evento MEStreamSinkRateChanged

Gerado por um sink de fluxo quando a taxa foi alterada.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Se um sink de fluxo dá suporte a alterações de taxa, ele envia esse evento depois que a alteração de taxa é concluída. O evento é enviado uma vez para cada chamada para o método [**IMFClockStateSink::OnClockSetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) do sink. Se a alteração de taxa não for bem-sucedida, o valor do status do evento será um código de erro.

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

 

 




