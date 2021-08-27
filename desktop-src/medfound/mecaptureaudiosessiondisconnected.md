---
description: enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão de WTS (serviços de Terminal do Windows).
ms.assetid: 88B24E79-FEB8-46AF-9A6C-3FB426089584
title: Evento MECaptureAudioSessionDisconnected (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 567df4839776ecacb5e25992f5f8cef4795186cffc53fb8abb433418066f3c40
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114166"
---
# <a name="mecaptureaudiosessiondisconnected-event"></a>Evento MECaptureAudioSessionDisconnected

enviado por uma origem de captura de áudio quando o dession de áudio é desconectado porque o usuário fez logoff de uma sessão de WTS (serviços de Terminal do Windows).

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> </dl>

 

 
