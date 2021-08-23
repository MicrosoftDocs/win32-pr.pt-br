---
title: MCIWNDM_CAN_SAVE mensagem (Vfw.h)
description: A mensagem MCIWNDM \_ CAN SAVE determina se um dispositivo \_ MCI pode salvar dados. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- MCIWNDM_CAN_SAVE mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccab622381208b8213414ed8b156a84e431afffc55acdf2323b0c0a2d31014f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429626"
---
# <a name="mciwndm_can_save-message"></a>Mensagem MCIWNDM \_ PODE \_ SALVAR

A **mensagem MCIWNDM \_ CAN \_ SAVE** determina se um dispositivo MCI pode salvar dados. Você pode enviar essa mensagem explicitamente ou usando a [**macro MCIWndCanSave.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** o dispositivo for compatível com salvar ou **FALSE** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





