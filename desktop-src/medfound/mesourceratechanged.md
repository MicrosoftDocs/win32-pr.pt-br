---
description: 'Gerado por uma origem de mídia quando a taxa de reprodução é alterada. Esse evento é enviado depois que o método IMFRateControl:: SetRate é concluído de forma assíncrona.'
ms.assetid: 68a7fe64-e28a-4c20-830c-9402e1fb57f8
title: Evento MESourceRateChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2af1ca671e09fc8a236ba79b36c1610635989ce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090701"
---
# <a name="mesourceratechanged-event"></a>Evento MESourceRateChanged

Gerado por uma origem de mídia quando a taxa de reprodução é alterada. Esse evento é enviado depois que o método [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) é concluído de forma assíncrona.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                                   |
|-------------------|-----------------------------------------------|
| VT \_ R4<br/> | A nova taxa de reprodução.<br/> <br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Implementando o controle de taxa](implementing-rate-control.md)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Controle de taxa](rate-control.md)
</dt> <dt>

[**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)
</dt> </dl>

 

 




