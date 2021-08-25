---
title: WM_CAP_GRAB_FRAME mensagem (Vfw.h)
description: A mensagem WM \_ CAP GRAB FRAME recupera e exibe um único quadro do driver de \_ \_ captura. Após a captura, a sobreposição e a visualização são desabilitadas. Você pode enviar essa mensagem explicitamente ou usando a macro capGrabFrame.
ms.assetid: 91d58c1c-53b9-4813-88c2-7a1acf641d96
keywords:
- WM_CAP_GRAB_FRAME mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- WM_CAP_GRAB_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdccfc9df0f3abac7febfa78029b4ecb351ec3044c618dc4c811e91b433f0f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892036"
---
# <a name="wm_cap_grab_frame-message"></a>Mensagem WM \_ CAP \_ GRAB \_ FRAME

A **mensagem WM CAP GRAB \_ \_ \_ FRAME** recupera e exibe um único quadro do driver de captura. Após a captura, a sobreposição e a visualização são desabilitadas. Você pode enviar essa mensagem explicitamente ou usando a [**macro capGrabFrame.**](/windows/desktop/api/Vfw/nf-vfw-capgrabframe)


```C++
WM_CAP_GRAB_FRAME 
wParam = (WPARAM)0; 
lParam = (LPARAM)0L; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** for bem-sucedido **ou FALSE** caso contrário.

## <a name="remarks"></a>Comentários

Para obter informações sobre como instalar funções de retorno de chamada, consulte as mensagens [**WM \_ CAP SET \_ \_ CALLBACK \_ ERROR**](wm-cap-set-callback-error.md) e [**WM CAP SET \_ \_ \_ CALLBACK \_ FRAME.**](wm-cap-set-callback-frame.md)

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

 

 





