---
title: WM_CAP_SINGLE_FRAME mensagem (Vfw.h)
description: A mensagem WM CAP SINGLE FRAME anexa um único quadro a um arquivo de captura que foi aberto usando a mensagem \_ WM CAP SINGLE FRAME \_ \_ \_ \_ \_ \_ OPEN. Você pode enviar essa mensagem explicitamente ou usando a macro capCaptureSingleFrame.
ms.assetid: 95466961-0719-4ff7-afc8-f7bf0e0974ac
keywords:
- WM_CAP_SINGLE_FRAME mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_SINGLE_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2080c8471849d42c2260c1f4133c996ef31e65e8a20591df531fbd24c19bc85c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891786"
---
# <a name="wm_cap_single_frame-message"></a>Mensagem WM \_ CAP \_ SINGLE \_ FRAME

A **mensagem WM CAP SINGLE \_ \_ \_ FRAME** anexa um único quadro a um arquivo de captura que foi aberto usando a mensagem [**WM CAP SINGLE FRAME \_ \_ \_ \_ OPEN.**](wm-cap-single-frame-open.md) Você pode enviar essa mensagem explicitamente ou usando a [**macro capCaptureSingleFrame.**](/windows/desktop/api/Vfw/nf-vfw-capcapturesingleframe)


```C++
WM_CAP_SINGLE_FRAME 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

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

 

 





