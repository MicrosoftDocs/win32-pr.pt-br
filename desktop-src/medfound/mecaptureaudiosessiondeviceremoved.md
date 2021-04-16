---
description: Enviado por uma fonte de captura de áudio quando o dispositivo é removido.
ms.assetid: A249D8B4-15A8-4AD3-8316-2886E5C37825
title: Evento MECaptureAudioSessionDeviceRemoved (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa0cf1b9a7536affed5a4665f6f2e364e1f872e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105765171"
---
# <a name="mecaptureaudiosessiondeviceremoved-event"></a>Evento MECaptureAudioSessionDeviceRemoved

Enviado por uma fonte de captura de áudio quando o dispositivo é removido.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE               | Descrição                           |
|-----------------------|---------------------------------------|
| VT \_ vazio <br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.

A origem de captura envia esse evento quando recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonDeviceRemoval**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
