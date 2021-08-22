---
title: Mensagem de WM_CAP_GET_AUDIOFORMAT (VFW. h)
description: A \_ \_ mensagem Get AUDIOFORMAT do WM Cap \_ Obtém o formato de áudio ou o tamanho do formato de áudio. Você pode enviar essa mensagem explicitamente ou usando as macros capGetAudioFormat e capGetAudioFormatSize.
ms.assetid: 25e58863-2b1e-4ed8-9f34-c39617a15bc1
keywords:
- mensagem de WM_CAP_GET_AUDIOFORMAT Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GET_AUDIOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d247c035f251b387537f8e6c360adf79e6ed479d8d40e4f8fe8180e059dab3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118940734"
---
# <a name="wm_cap_get_audioformat-message"></a>\_Mensagem de \_ Get \_ AUDIOFORMAT do WM Cap

A **mensagem \_ \_ Get \_ AUDIOFORMAT do WM Cap** Obtém o formato de áudio ou o tamanho do formato de áudio. Você pode enviar essa mensagem explicitamente ou usando as macros [**capGetAudioFormat**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformat) e [**capGetAudioFormatSize**](/windows/desktop/api/Vfw/nf-vfw-capgetaudioformatsize) .


```C++
WM_CAP_GET_AUDIOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (LPWAVEFORMATEX) (psAudioFormat); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*wSize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="psAudioFormat"></span><span id="psaudioformat"></span><span id="PSAUDIOFORMAT"></span>*psAudioFormat*
</dt> <dd>

Ponteiro para uma estrutura [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) ou **NULL**. Se o valor for **NULL**, o tamanho, em bytes, necessário para manter a estrutura será retornado.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retorna o tamanho, em bytes, do formato de áudio.

## <a name="remarks"></a>Comentários

Como os formatos de áudio compactados variam em requisitos de tamanho, os aplicativos devem primeiro recuperar o tamanho, depois alocar memória e, por fim, solicitar os dados do formato de áudio.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

