---
description: Gerado pelo processador de áudio quando o formato de áudio padrão para o dispositivo de áudio é alterado. O processador de áudio agora é inválido.
ms.assetid: eeef764a-f6d2-4f6e-9af3-acd5fd7bc55c
title: Evento MEAudioSessionFormatChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0464aa4bd98ec0143838762ac3fcc3efd88e03528b1d5732e2d5423a711640
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013866"
---
# <a name="meaudiosessionformatchanged-event"></a>Evento MEAudioSessionFormatChanged

Gerado pelo processador de áudio quando o formato de áudio padrão para o dispositivo de áudio é alterado. O processador de áudio agora é inválido.

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vazio<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo coletor de fluxo do processador de áudio. O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnSessionDisconnected**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-onsessiondisconnected) da sessão de áudio do modo de usuário com o motivo de desconexão igual a **DisconnectReasonFormatChanged**.

O ponteiro [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) , se definido, não é útil, pois o fluxo de áudio não é mais válido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
