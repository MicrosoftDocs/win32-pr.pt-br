---
description: Gerado pelo renderador de áudio quando o sistema Windows de áudio é desligado. O renderador de áudio agora é inválido.
ms.assetid: 8e80903c-d6ce-4fa2-87db-552c7fba3c6a
title: Evento MEAudioSessionServerShutdown (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ca1f9a4aa9e2ba0e9c57b21a45aa3806a8538e3e81cb16a2f208677d78cbacf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062428"
---
# <a name="meaudiosessionservershutdown-event"></a>Evento MEAudioSessionServerShutdown

Gerado pelo renderador de áudio quando o sistema Windows de áudio é desligado. O renderador de áudio agora é inválido.

A Sessão de Mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ VAZIO<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo sink de fluxo do renderador de áudio. O evento é disparado quando o renderizador de áudio recebe um evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a **DisconnectReasonServerShutdown**.

O [**ponteiro IMFAudioPolicy,**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) se definido, não é útil, porque o fluxo de áudio não é mais válido.

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

[Renderização de áudio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
