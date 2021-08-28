---
description: Enviado pelo IMFMediaSource que encapsula o dispositivo para indicar que o dispositivo foi removido.
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: Evento MEVideoCaptureDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f209dc4be6e8f45639b060de1328cb04c932463f6b76355b7538b5649a69634e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013476"
---
# <a name="mevideocapturedeviceremoved-event"></a>Evento MEVideoCaptureDeviceRemoved

Enviado pelo [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula o dispositivo para indicar que o dispositivo foi removido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE               | Descrição                           |
|-----------------------|---------------------------------------|
| VT \_ vazio <br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) que encapsula o dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 




