---
description: Gerado pelo processador de áudio quando os parâmetros de agrupamento mudam para a sessão de áudio.
ms.assetid: d6f7757c-fd91-40bd-b2b5-a3e808445250
title: Evento MEAudioSessionGroupingParamChanged (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab9a271ebaa4e3a0044dc425de2d6a7f313e17d63c693acede63773e94619c6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957506"
---
# <a name="meaudiosessiongroupingparamchanged-event"></a>Evento MEAudioSessionGroupingParamChanged

Gerado pelo processador de áudio quando os parâmetros de agrupamento mudam para a sessão de áudio.

A sessão de mídia encaminha esse evento para o aplicativo.

## <a name="event-values"></a>Valores de evento

Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.



| VARTYPE                | Descrição                                                                               |
|------------------------|-------------------------------------------------------------------------------------------|
| VT \_ desconhecido<br/> | Ponteiro para a interface [**IMFAudioPolicy**](/windows/desktop/api/mfidl/nn-mfidl-imfaudiopolicy) .<br/> <br/> |



## <a name="remarks"></a>Comentários

Esse evento é enviado pelo coletor de fluxo do processador de áudio. O evento é disparado quando o processador de áudio recebe um evento [**IAudioSessionEvents:: OnGroupingParamChanged**](/windows/win32/api/audiopolicy/nf-audiopolicy-iaudiosessionevents-ongroupingparamchanged) da sessão de áudio.

Para obter os novos parâmetros de agrupamento, chame [**IMFAudioPolicy:: GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam).

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

[**IMFAudioPolicy::GetGroupingParam**](/windows/desktop/api/mfidl/nf-mfidl-imfaudiopolicy-getgroupingparam)
</dt> <dt>

[Processador de streaming de áudio](streaming-audio-renderer.md)
</dt> </dl>

 

 
