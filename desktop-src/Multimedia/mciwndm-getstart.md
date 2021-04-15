---
title: Mensagem de MCIWNDM_GETSTART (VFW. h)
description: A \_ mensagem GETstart MCIWNDM recupera o local do início do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetStart.
ms.assetid: 2350616c-2aac-4ff6-b074-bb785a97cdfb
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSTART
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
ms.openlocfilehash: 63cbe88df006f1f98854e42259074d82bbd87dc1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454749"
---
# <a name="mciwndm_getstart-message"></a>MCIWNDM \_ getiniciar mensagem

A **mensagem \_ GetStart MCIWNDM** recupera o local do início do conteúdo de um dispositivo ou arquivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) .


```C++
MCIWNDM_GETSTART 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o local no formato de hora atual.

## <a name="remarks"></a>Comentários

Normalmente, o valor de retorno é zero; Mas alguns dispositivos usam um local de início diferente de zero. A busca desse local define o dispositivo para o início da mídia.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart)
</dt> </dl>

 

 





