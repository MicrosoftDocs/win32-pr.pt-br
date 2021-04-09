---
description: Enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão do WTS (serviços de terminal do Windows).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dae45ecded4a2a412525da70133845c2487aa604
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090814"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>Evento MECaptureAudioSessionDisconnected

Enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão do WTS (serviços de terminal do Windows).

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE               | Descrição                           |
|-----------------------|---------------------------------------|
| VT \_ vazio <br/> | Nenhum dado do evento.<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo fluxo de mídia da fonte de captura de áudio.

A origem de captura envia esse evento quando recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonSessionDisconnected**.

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

 

 
