---
title: Mensagem de ICM_DRAW_STOP (VFW. h)
description: A \_ mensagem de parada de desenho ICM \_ Notifica um driver de renderização para interromper seu relógio interno durante o período de desenho de quadros. Você pode enviar essa mensagem explicitamente ou usando a macro ICDrawStop.
ms.assetid: 9ffda595-e3d6-48f0-9487-69f7e95979c2
keywords:
- Multimídia do Windows de mensagem ICM_DRAW_STOP
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
ms.openlocfilehash: b3bde99dfcf483e67aa6a601de2718814cc22439
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454989"
---
# <a name="icm_draw_stop-message"></a>Mensagem de parada de \_ desenho ICM \_

A mensagem de **\_ \_ parada de desenho ICM** notifica um driver de renderização para interromper seu relógio interno durante o período de desenho de quadros. Você pode enviar essa mensagem explicitamente ou usando a macro [**ICDrawStop**](/windows/desktop/api/Vfw/nf-vfw-icdrawstop) .


```C++
ICM_DRAW_STOP 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="remarks"></a>Comentários

Essa mensagem é usada por hardware que executa sua própria descompactação assíncrona, tempo e desenho.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Gerenciador de compactação de vídeo](video-compression-manager.md)
</dt> <dt>

[Mensagens de compactação de vídeo](video-compression-messages.md)
</dt> </dl>

 

 





