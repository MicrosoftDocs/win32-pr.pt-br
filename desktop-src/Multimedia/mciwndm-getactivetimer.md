---
title: Mensagem de MCIWNDM_GETACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM GETACTIVETIMER recupera o período de atualização usado quando a janela MCIWnd é a janela ativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- mensagem de MCIWNDM_GETACTIVETIMER Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc542e5a4b43b974eb7f28bc59d8e2fab7547834f28b5bccb6ea46f978e2158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525516"
---
# <a name="mciwndm_getactivetimer-message"></a>\_Mensagem MCIWNDM GETACTIVETIMER

A mensagem **MCIWNDM \_ GETACTIVETIMER** recupera o período de atualização usado quando a janela MCIWnd é a janela ativa. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer) .


```C++
MCIWNDM_GETACTIVETIMER 
wParam = 0; 
lParam = 0L; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o período de atualização em milissegundos. O padrão é 500 milissegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetactivetimer)
</dt> </dl>

 

 





