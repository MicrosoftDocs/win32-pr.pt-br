---
title: WM_CAP_SET_VIDEOFORMAT mensagem (Vfw.h)
description: A mensagem WM \_ CAP \_ SET \_ VIDEOFORMAT define o formato dos dados de vídeo capturados. Você pode enviar essa mensagem explicitamente ou usando a macro capSetVideoFormat.
ms.assetid: 4f9cf90d-7ccb-4fc7-aad5-3d7e082526be
keywords:
- WM_CAP_SET_VIDEOFORMAT mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SET_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c543f613fedf54518579829d6825bd20dc4738ae03cb77f0996f8a58a123cb76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135008"
---
# <a name="wm_cap_set_videoformat-message"></a>Mensagem WM \_ CAP \_ SET \_ VIDEOFORMAT

A **mensagem WM CAP SET \_ \_ \_ VIDEOFORMAT** define o formato dos dados de vídeo capturados. Você pode enviar essa mensagem explicitamente ou usando a [**macro capSetVideoFormat.**](/windows/desktop/api/Vfw/nf-vfw-capsetvideoformat)


```C++
WM_CAP_SET_VIDEOFORMAT 
wParam = (WPARAM) (wSize); 
lParam = (LPARAM) (LPVOID) (psVideoFormat); 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="wSize"></span><span id="wsize"></span><span id="WSIZE"></span>*Wsize*
</dt> <dd>

Tamanho, em bytes, da estrutura referenciada por **s**.

</dd> <dt>

<span id="psVideoFormat"></span><span id="psvideoformat"></span><span id="PSVIDEOFORMAT"></span>*psVideoFormat*
</dt> <dd>

Ponteiro para uma [**estrutura BITMAPINFO.**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo)

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Como os formatos de vídeo são específicos do dispositivo, os aplicativos devem verificar o valor de retorno dessa função para determinar se o formato é aceito pelo driver.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Captura de vídeo](video-capture.md)
</dt> <dt>

[Mensagens de captura de vídeo](video-capture-messages.md)
</dt> </dl>

 

