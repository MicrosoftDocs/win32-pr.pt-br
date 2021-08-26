---
title: ICM_DRAW_STOP mensagem (Vfw.h)
description: A ICM DRAW STOP notifica um driver de renderização para interromper seu relógio interno \_ para o tempo dos quadros de \_ desenho. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- ICM_DRAW_STOP mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- ICM_DRAW_STOP
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41bdb8fbc9a0cddf470733fa35b2f25dc62675175cbb40c427d0b160074c5409
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038786"
---
# <a name="icm_draw_stop-message"></a>\_ICM Mensagem DRAW \_ STOP

A **ICM \_ DRAW \_ STOP** notifica um driver de renderização para interromper seu relógio interno para o tempo dos quadros de desenho. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStop.**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop)


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é usada pelo hardware que executa sua própria descompactação, tempo e desenho assíncronos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de Compactação de Vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





