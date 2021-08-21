---
title: Mensagem de WM_CAP_SINGLE_FRAME_OPEN (VFW. h)
description: A \_ mensagem aberta do quadro do WM Cap \_ \_ \_ abre o arquivo de captura para a captura de um único quadro. Todas as informações anteriores no arquivo de captura são substituídas. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrameOpen.
ms.assetid: 4814737c-4395-4c01-a68e-fac43dd291fd
keywords:
- mensagem de WM_CAP_SINGLE_FRAME_OPEN Windows multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME_OPEN
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a58df70bea8971e10a769efbbc98220c46897ff6979e66ab45ae8f2ba81b971
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118134831"
---
# <a name="wm_cap_single_frame_open-message"></a>\_Mensagem de \_ \_ abertura de quadro único \_ do WM Cap

A **mensagem \_ \_ aberta do \_ quadro \_ do WM Cap** abre o arquivo de captura para a captura de um único quadro. Todas as informações anteriores no arquivo de captura são substituídas. Você pode enviar essa mensagem explicitamente ou usando a macro [**capCaptureSingleFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframeopen) .


```C++
WM_CAP_SINGLE_FRAME_OPEN 
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

 

 





