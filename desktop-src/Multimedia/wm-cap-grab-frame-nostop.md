---
title: Mensagem de WM_CAP_GRAB_FRAME_NOSTOP (VFW. h)
description: A \_ mensagem nostop do quadro de captura da Cap do WM \_ \_ \_ preenche o buffer do quadro com um único quadro descompactado do dispositivo de captura e o exibe.
ms.assetid: 5f6e3ce7-3595-456e-82c8-eeb162ace81a
keywords:
- mensagem de WM_CAP_GRAB_FRAME_NOSTOP Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME_NOSTOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b81c581ad7e3913640271b32b18791ebf7b48ed09cd365af82ed263449f05471
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622595"
---
# <a name="wm_cap_grab_frame_nostop-message"></a>\_ \_ \_ Mensagem nostop do quadro de captura da Cap do WM \_

A **mensagem \_ \_ \_ \_ nostop do quadro de captura da Cap do WM** preenche o buffer do quadro com um único quadro descompactado do dispositivo de captura e o exibe. Ao contrário da mensagem do quadro de captura da Cap do WM, o estado da sobreposição ou da visualização não é alterado por essa mensagem. [**\_ \_ \_**](wm-cap-grab-frame.md) Você pode enviar essa mensagem explicitamente ou usando a macro [**capGrabFrameNoStop**](/windows/desktop/api/Vfw/nf-vfw-capgrabframenostop) .


```C++
WM_CAP_GRAB_FRAME_NOSTOP 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

Para obter informações sobre como instalar funções de chamada de retorno, consulte as mensagens de quadro de retorno de chamada do [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-error.md) e [**WM \_ Cap \_ set \_ callback \_**](wm-cap-set-callback-frame.md) .

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

 

 





