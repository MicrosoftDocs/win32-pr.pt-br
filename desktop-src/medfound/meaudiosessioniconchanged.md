---
description: Gerado pelo processador de áudio quando o ícone de sessão de áudio é alterado.
ms.assetid: 72aae901-e5fe-481d-babb-459038abd629
title: Evento MEAudioSessionIconChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba7a12a4e82585c270206d595d32ba82c4e9e594
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105788798"
---
# <a name="meaudiosessioniconchanged-event"></a>Evento MEAudioSessionIconChanged

Gerado pelo processador de áudio quando o ícone de sessão de áudio é alterado.

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ vazio<br/>   | Nenhum dado do evento.<br/> <br/>                                                     |
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo coletor de fluxo do processador de áudio. O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnIconPathChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-oniconpathchanged) da sessão de áudio.

Para obter o novo ícone, chame [**IMFAudioPolicy:: GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Mfobjects. h (incluir Mfidl. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMFAudioPolicy::GetIconPath**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-geticonpath)
</dt> <dt>

[Eventos de Media Foundation](media-foundation-events.md)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
