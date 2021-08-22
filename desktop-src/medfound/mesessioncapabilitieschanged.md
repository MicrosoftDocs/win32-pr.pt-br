---
description: Gerado pela Sessão de Mídia quando os recursos de sessão são alterados.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc97cb5168957f34cc029a982447c6d4775075ea6f9b9b250ce7b9fd7f1791d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119464866"
---
# <a name="mesessioncapabilitieschanged-event"></a>Evento MESessionCapabilitiesChanged

Gerado pela Sessão de Mídia quando os recursos de sessão são alterados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ VAZIO<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

O evento contém os atributos a seguir.



| Atributo                                                                     | Descrição                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_ \_ SESSIONCAPS DE EVENTO MF**](mf-event-sessioncaps-attribute.md)              | Novos sinalizadores de funcionalidades de sessão.                  |
| [**DELTA \_ \_ SESSIONCAPS DO EVENTO MF \_**](mf-event-sessioncaps-delta-attribute.md) | Indica quais sinalizadores de funcionalidades foram alterados. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




