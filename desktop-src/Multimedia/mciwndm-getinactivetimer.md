---
title: Mensagem de MCIWNDM_GETINACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM GETINACTIVETIMER recupera o período de atualização usado quando a janela MCIWnd é a janela inativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetInactiveTimer.
ms.assetid: 84e00d2f-2cf8-4b6b-a8cb-7eb320754783
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETINACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_GETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a270aeffdee59b7749aa87a0e711204960d74d7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105810307"
---
# <a name="mciwndm_getinactivetimer-message"></a>\_Mensagem MCIWNDM GETINACTIVETIMER

A mensagem **MCIWNDM \_ GETINACTIVETIMER** recupera o período de atualização usado quando a janela MCIWnd é a janela inativa. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer) .


```C++
MCIWNDM_GETINACTIVETIMER 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o período de atualização, em milissegundos. O valor padrão é 2000 milissegundos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetinactivetimer)
</dt> </dl>

 

 





