---
title: Mensagem de MCIWNDM_GETREPEAT (VFW. h)
description: A \_ mensagem MCIWNDM getrepetir determina se a reprodução contínua foi ativada. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetRepeat.
ms.assetid: 6d644117-e705-421f-b45f-9f0e833e6bc8
keywords:
- mensagem de MCIWNDM_GETREPEAT Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_GETREPEAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5045f56f2d189884e6d2dee978ec8800fa9c24c3ff01fc3fe93680b4ae7f53af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374193"
---
# <a name="mciwndm_getrepeat-message"></a>MCIWNDM \_ getrepetir mensagem

A mensagem **MCIWNDM \_ getrepetir** determina se a reprodução contínua foi ativada. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat) .


```C++
MCIWNDM_GETREPEAT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se a reprodução contínua for ativada ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetRepeat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetrepeat)
</dt> </dl>

 

 





