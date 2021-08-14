---
title: Mensagem de MCIWNDM_GETLENGTH (VFW. h)
description: A \_ mensagem MCIWNDM GETLENGTH recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetLength.
ms.assetid: bee4d9fc-78eb-4577-98bb-d6c2d9acbb7f
keywords:
- mensagem de MCIWNDM_GETLENGTH Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETLENGTH
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 334d9a4a62171a62cbd0fc914be2d9a81ed901eab6d3893170cb8dabd2426a36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374183"
---
# <a name="mciwndm_getlength-message"></a>\_Mensagem MCIWNDM GETLENGTH

A mensagem **MCIWNDM \_ GETLENGTH** recupera o tamanho do conteúdo ou arquivo usado atualmente por um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) .


```C++
MCIWNDM_GETLENGTH 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o comprimento. As unidades para o comprimento dependem do formato de hora atual.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetLength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength)
</dt> </dl>

 

 





