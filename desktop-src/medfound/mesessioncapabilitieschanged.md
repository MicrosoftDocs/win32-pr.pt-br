---
description: Gerado pela sessão de mídia quando os recursos de sessão são alterados.
ms.assetid: d59fd3a0-29db-434c-b6ba-d9beb33bd965
title: Evento MESessionCapabilitiesChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0612b705571c50a6adcbde4afe93b42a524a950
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766507"
---
# <a name="mesessioncapabilitieschanged-event"></a>Evento MESessionCapabilitiesChanged

Gerado pela sessão de mídia quando os recursos de sessão são alterados.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE              | Descrição                           |
|----------------------|---------------------------------------|
| VT \_ vazio<br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

O evento contém os atributos a seguir.



| Atributo                                                                     | Descrição                                      |
|-------------------------------------------------------------------------------|--------------------------------------------------|
| [**\_SESSIONCAPS do evento MF \_**](mf-event-sessioncaps-attribute.md)              | Sinalizadores de novas funcionalidades de sessão.                  |
| [**\_ \_ SESSIONCAPS Delta de evento MF \_**](mf-event-sessioncaps-delta-attribute.md) | Indica quais sinalizadores de funcionalidades foram alterados. |



 

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

 

 




