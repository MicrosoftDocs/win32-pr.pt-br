---
description: Gerado pela Sessão de Mídia quando o status de uma topologia muda.
ms.assetid: b45fd598-ab1e-4b12-8d82-c88c96d1f770
title: Evento MESessionTopologyStatus (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42adfd1a86319f65077e87925eb23807253f12b06e977ee1eb9e494a4c7df180
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119723716"
---
# <a name="mesessiontopologystatus-event"></a>Evento MESessionTopologyStatus

Gerado pela Sessão de Mídia quando o status de uma topologia muda.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                                         |
|------------------------|-----------------------------------------------------------------------------------------------------|
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) da topologia.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para esse evento.



| Atributo                                                                            | Descrição                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**STATUS DA \_ TOPOLOGIA DE \_ \_ EVENTO MF**](mf-event-topology-status-attribute.md)<br/> | Especifica o novo status da topologia.<br/> <br/> |



## <a name="remarks"></a>Comentários

Para obter um exemplo de código que recupera o ponteiro [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) do evento, consulte [Evento MESessionTopologySet.](mesessiontopologyset.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




