---
title: MCIWNDM_GETSTART mensagem (Vfw.h)
description: A mensagem GETSTART MCIWNDM recupera o local do início do conteúdo de um dispositivo \_ ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- MCIWNDM_GETSTART mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETSTART
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0efb5689009fdd6928afd1d2f232bcb1bbeb2160aecf3d79ddb263ed6f315de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429226"
---
# <a name="mciwndm_getstart-message"></a>Mensagem GETSTART MCIWNDM \_

A **mensagem \_ GETSTART MCIWNDM** recupera o local do início do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a [**macro MCIWndGetStart.**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o local no formato de hora atual.

## <a name="remarks"></a>Comentários

Normalmente, o valor de retorno é zero; mas alguns dispositivos usam um local inicial diferente de zero. Buscar esse local define o dispositivo como o início da mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





