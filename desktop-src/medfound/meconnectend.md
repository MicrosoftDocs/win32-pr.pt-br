---
description: Gerado pela origem da rede quando termina de abrir uma URL.
ms.assetid: 737aec32-24f4-4825-ad34-8d2fc889bc09
title: Evento MEConnectEnd (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9801b1af38f7bf0a0107680d77a399b3927a616e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812125"
---
# <a name="meconnectend-event"></a>Evento MEConnectEnd

Gerado pela origem da rede quando termina de abrir uma URL.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Description                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

A origem da rede envia esse evento diretamente para o aplicativo por meio do método [**IMFSourceOpenMonitor:: OnSourceEvent**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceopenmonitor-onsourceevent) do aplicativo, não por meio da interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) usual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFSourceOpenMonitor**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceopenmonitor)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




