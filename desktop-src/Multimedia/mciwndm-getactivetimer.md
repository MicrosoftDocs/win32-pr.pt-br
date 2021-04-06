---
title: Mensagem de MCIWNDM_GETACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM GETACTIVETIMER recupera o período de atualização usado quando a janela MCIWnd é a janela ativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetActiveTimer.
ms.assetid: f9e6f9ed-75fd-4e45-ad92-79a82d8d572c
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETACTIVETIMER
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
ms.openlocfilehash: 4cb86fc2940c8bd5d82c004754b81e5389ada892
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086506"
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

 

 





