---
description: Gerados pelos sinks de fluxo do EVR (renderador de vídeo aprimorado) se o dispositivo de vídeo mudar.
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: Evento MEStreamSinkDeviceChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb760a45125ae7434ff2a58d43f087d2ec3c030cb29351ea4d2113ca8fe10c0a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061006"
---
# <a name="mestreamsinkdevicechanged-event"></a>Evento MEStreamSinkDeviceChanged

Gerados pelos sinks de fluxo do EVR (renderador de vídeo aprimorado) se o dispositivo de vídeo mudar. Por exemplo, o EVR gera esse evento quando recebe um evento [**EC \_ DISPLAY \_ CHANGED.**](../directshow/ec-display-changed.md)

O Media Foundation pipeline responde a esse evento reemitindo todas as solicitações de exemplo que falharam durante a alteração do dispositivo.

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

 

 
