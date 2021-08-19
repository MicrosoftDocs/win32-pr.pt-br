---
description: Gerado pelo renderador de áudio quando o ícone de sessão de áudio é muda.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ce466cf88b93c9cf806a2a6b70f76b084e8aa0b2c8fb2910a7391337a13b2f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118062455"
---
# <a name="meaudiosessioniconchanged-event"></a>Evento MEAudioSessionIconChanged

Gerado pelo renderador de áudio quando o ícone de sessão de áudio é muda.

A Sessão de Mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| Vartype                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ VAZIO<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ UNKNOWN<br/> | Ponteiro para a interface [**IMFAudioPolicy.**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy)<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo sink de fluxo do renderador de áudio. O evento é disparado quando o renderador de áudio recebe um [**evento IAudioSessionEvents::OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) da sessão de áudio.

Para obter o novo ícone, chame [**IMFAudioPolicy::GetIconPath.**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects.h (inclua Mfidl.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Media Foundation eventos](media-foundation-events.md)
</dt> <dt>

[Renderização de áudio de streaming](streaming-audio-renderer.md)
</dt> </dl>

 

 
