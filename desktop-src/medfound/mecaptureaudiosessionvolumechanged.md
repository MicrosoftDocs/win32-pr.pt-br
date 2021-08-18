---
description: Enviado por uma fonte de captura de áudio quando o volume muda.
ms.assetid: 4A525D5F-9226-4277-BDB7-174BF65FE320
title: Evento MECaptureAudioSessionVolumeChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f2e83bdf03f61abac733a5e06310ff12c0797664d6a2405aed97210bf5ff42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878073"
---
# <a name="mecaptureaudiosessionvolumechanged-event"></a>Evento MECaptureAudioSessionVolumeChanged

Enviado por uma fonte de captura de áudio quando o volume muda.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype               | Descrição                           |
|-----------------------|---------------------------------------|
| VT \_ VAZIO <br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.

A fonte de captura de áudio envia esse evento se uma ação externa altera o volume , por exemplo, se o usuário altera o volume por meio do Painel de Controle. A origem da captura não enviará o evento se o aplicativo mudar o volume diretamente na origem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> </dl>

 

 




