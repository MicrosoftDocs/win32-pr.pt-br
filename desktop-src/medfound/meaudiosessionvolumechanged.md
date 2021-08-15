---
description: Enviado pelo processamento de áudio de streaming (SAR) quando o estado de volume ou mudo da sessão de áudio for alterado.
ms.assetid: 63c37bd2-0289-407a-92f1-169eb5d2e02e
title: Evento MEAudioSessionVolumeChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 721de9751cac284cb25d390d948f0f686447c04eaa613c1fecd4bf3503bce76d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119465396"
---
# <a name="meaudiosessionvolumechanged-event"></a>Evento MEAudioSessionVolumeChanged

Enviado pelo processamento de áudio de streaming (SAR) quando o estado de volume ou mudo da sessão de áudio for alterado.

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vazio<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é gerado pelo coletor de fluxo do SAR. O evento é disparado quando o SAR recebe um evento [**IAudioSessionEvents:: OnSimpleVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsimplevolumechanged) da sessão de áudio. Para obter o novo nível de volume e o estado de mudo, chame [**IMFSimpleAudioVolume:: GetMasterVolume**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmastervolume) e [**IMFSimpleAudioVolume:: getmudo**](/windows/desktop/api/mfidl/nf-mfidl-imfsimpleaudiovolume-getmute).

O SAR envia esse evento se uma ação externa alterar o volume — por exemplo, se o usuário alterar o volume por meio do SndVol (programa de controle de volume de sistema). O SAR não enviará o evento se o aplicativo alterar o volume diretamente no SAR.

Além disso, o SAR não envia esse evento quando o volume do canal é alterado ([**IAudioSessionEvents:: OnChannelVolumeChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onchannelvolumechanged)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
