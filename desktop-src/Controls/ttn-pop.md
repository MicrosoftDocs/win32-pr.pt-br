---
title: TTN_POP de notificação (Commctrl.h)
description: Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 44a38f1a-f1df-4057-bf76-f87eb467f0d7
keywords:
- TTN_POP de notificação Windows Controles
topic_type:
- apiref
api_name:
- TTN_POP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3322da3ddbb677631a433e4cce1d2a9eb6e56c3484314026242f23c91c103f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109476"
---
# <a name="ttn_pop-notification-code"></a>Código de notificação \_ POP TTN

Notifica a janela do proprietário de que uma dica de ferramenta está prestes a ser ocultada. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TTN_POP

    pnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMHDR.**](/windows/desktop/api/richedit/ns-richedit-nmhdr)

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





