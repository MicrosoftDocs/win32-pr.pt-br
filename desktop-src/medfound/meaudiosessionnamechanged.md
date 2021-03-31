---
description: Gerado pelo processador de áudio quando o nome de exibição da sessão de áudio é alterado.
ms.assetid: d180b145-88e1-4f85-b001-b76140ca39d8
title: Evento MEAudioSessionNameChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb06244c196ab55bbd93e12ebff6a6a394176cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647494"
---
# <a name="meaudiosessionnamechanged-event"></a>Evento MEAudioSessionNameChanged

Gerado pelo processador de áudio quando o nome de exibição da sessão de áudio é alterado.

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo coletor de fluxo do processador de áudio. O evento é disparado quando o renderizador de áudio recebe um evento [**IAudioSessionEvents:: Ondisplaynamechanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ondisplaynamechanged) da sessão de áudio.

Para obter o novo nome de exibição, chame [**IMFAudioPolicy:: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFAudioPolicy:: GetDisplayName**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getdisplayname)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
