---
title: Mensagem de MCIWNDM_GETZOOM (VFW. h)
description: A \_ mensagem getzoom do MCIWNDM recupera o valor de zoom atual usado por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetZoom.
ms.assetid: 92db8df2-515a-4616-a0f5-245d466ba379
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETZOOM
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
ms.openlocfilehash: fcb4ae1883787f1b86dcc17f2d4a3e0e0ee29ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454983"
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

 

 





