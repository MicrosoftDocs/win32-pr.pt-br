---
description: 'Gerado por uma fonte de mídia para solicitar uma nova taxa de reprodução. O aplicativo deve chamar IMFRateControl:: SetRate com a taxa solicitada. Uma fonte de mídia poderá gerar esse evento se não for possível continuar a reprodução na taxa atual.'
ms.assetid: 705e5a79-836b-417b-a7ed-c733572f6905
title: Evento MESourceRateChangeRequested (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7d8a88225fd3a0a95c56d549a712b295ba562cc684c08fe4b762c0169e3637c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974125"
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
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




