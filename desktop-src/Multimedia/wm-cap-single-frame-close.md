---
title: Mensagem de WM_CAP_SINGLE_FRAME_CLOSE (VFW. h)
description: A mensagem de fechamento do quadro do WM \_ Cap \_ \_ \_ fecha o arquivo de captura aberto \_ pela \_ mensagem de abertura de quadro único do WM Cap \_ \_ . Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrameClose.
ms.assetid: fde5f34b-0781-49a2-a509-64192a1d9ec0
keywords:
- mensagem de WM_CAP_SINGLE_FRAME_CLOSE Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_CLOSE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f304fd0c62818562e53c6129a15b266db6f1ac000de64fb779e5cdb3e437d43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134960"
---
# <a name="wm_cap_single_frame_close-message"></a>\_Mensagem de \_ \_ fechamento do quadro único \_ do WM Cap

A mensagem de **\_ fechamento do \_ \_ quadro \_ do WM Cap** fecha o arquivo de captura aberto pela mensagem de [**\_ \_ \_ \_ abertura de quadro único do WM Cap**](wm-cap-single-frame-open.md) . Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrameClose**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeclose) .


```C++
WM_CAP_SINGLE_FRAME_CLOSE 
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

 

 





