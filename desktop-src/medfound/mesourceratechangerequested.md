---
description: 'Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução. O aplicativo deve chamar IMFRateControl:: SetRate com a taxa solicitada. Uma fonte de mídia poderá gerar esse evento se não for possível continuar a reprodução na taxa atual.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9973a509541f3ec3d4f6a235b8f1277a20f7ed1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165038"
---
# <a name="mesourceratechangerequested-event"></a>Evento MESourceRateChangeRequested

Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução. O aplicativo deve chamar [**IMFRateControl:: SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) com a taxa solicitada. Uma fonte de mídia poderá gerar esse evento se não for possível continuar a reprodução na taxa atual.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE           | Descrição                                             |
|-------------------|---------------------------------------------------------|
| VT \_ R4<br/> | A nova taxa de reprodução solicitada.<br/> <br/> |



## <a name="attributes"></a>Atributos

Os atributos a seguir são definidos para este evento.



| Atributo                                                                    | Descrição                                                                       |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**o \_ evento MF \_ faz a \_ finação**](mf-event-do-thinning-attribute.md)<br/> | Especifica se a origem da mídia também solicita a fina.<br/> <br/> |



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

 

 




