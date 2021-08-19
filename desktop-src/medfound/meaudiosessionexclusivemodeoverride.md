---
description: Gerado pelo renderador de áudio quando a sessão de áudio é preempção por uma conexão de modo exclusivo. O renderador de áudio agora é inválido.
ms.assetid: f89acfe4-14a7-4051-a816-e5e0ba8db80a
title: Evento MEAudioSessionExclusiveModeOverride (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6344a5d073e9dc29777e6cb181c77bcae79da8602b830ade86646459e4d0bea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114216"
---
# <a name="meaudiosessionexclusivemodeoverride-event"></a>Evento MEAudioSessionExclusiveModeOverride

Gerado pelo renderador de áudio quando a sessão de áudio é preempção por uma conexão de modo exclusivo. O renderador de áudio agora é inválido.

A Sessão de Mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ VAZIO<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo sink de fluxo do renderador de áudio. O evento é disparado quando o renderizador de áudio recebe um evento [**IAudioSessionEvents::OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio com o motivo de desconexão igual a DisconnectReasonExclusiveModeOverride.

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

 

 
