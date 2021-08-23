---
title: MCIWNDM_EJECT mensagem (Vfw.h)
description: A mensagem MCIWNDM \_ EJECT envia um comando a um dispositivo MCI para ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndEject.
ms.assetid: a492f504-8b58-480e-9766-bc2878466c44
keywords:
- MCIWNDM_EJECT mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c752f192e8f74f2c6e861e581fd22a561bafd9ff6c0f369ba669bc4bf87fb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429426"
---
# <a name="mciwndm_eject-message"></a>Mensagem MCIWNDM \_ EJETO

A **mensagem MCIWNDM \_ EJECT envia** um comando a um dispositivo MCI para ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndEject.**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)


```C++
MCIWNDM_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndeject)
</dt> </dl>

 

 





