---
title: Mensagem de MCIWNDM_GETZOOM (VFW. h)
description: A \_ mensagem getzoom do MCIWNDM recupera o valor de zoom atual usado por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- mensagem de MCIWNDM_GETZOOM Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETZOOM
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52c247230ffe6269f77b906d874a4cf82a21ed8d3388ffa18193417603e45fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374137"
---
# <a name="mciwndm_getzoom-message"></a>\_Mensagem GETzoom do MCIWNDM

A **mensagem \_ Getzoom do MCIWNDM** recupera o valor de zoom atual usado por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom) .


```C++
MCIWNDM_GETZOOM 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna os valores mais recentes usados com [**MCIWNDM \_ setZoom**](mciwndm-setzoom.md).

## <a name="remarks"></a>Comentários

Um valor de retorno de 100 indica que a imagem não está ampliada. Um valor de 200 indica que a imagem é ampliada para duas vezes seu tamanho original. Um valor de 50 indica que a imagem é reduzida para metade do tamanho original.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetZoom**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetzoom)
</dt> <dt>

[**MCIWNDM \_ SETzoom**](mciwndm-setzoom.md)
</dt> </dl>

 

 





