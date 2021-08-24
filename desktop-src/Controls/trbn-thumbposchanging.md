---
title: TRBN_THUMBPOSCHANGING de notificação (Commctrl.h)
description: Notifica que a posição do polegar em uma barra de faixa está mudando. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 0876e026-bc07-409d-b174-b97ed704fc11
keywords:
- TRBN_THUMBPOSCHANGING código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TRBN_THUMBPOSCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48f05f67eb20c78f764957e73d2293d32e88f25a73d44d6b58f9a1c310b8d9d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751036"
---
# <a name="trbn_thumbposchanging-notification-code"></a>TRBN \_ THUMBPOSCHANGING notification code

Notifica que a posição do polegar em uma barra de faixa está mudando. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
TRBN_THUMBPOSCHANGING

    lpNMTrbThumbPosChanging = (NMTRBTHUMBPOSCHANGING*) lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMTRBTHUMBPOSCHANGING.**](/windows/win32/api/commctrl/ns-commctrl-nmtrbthumbposchanging) O chamador é responsável por alocar essa estrutura e definir seus membros, incluindo os membros da estrutura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) contida.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorne **TRUE** para impedir que o polegar se move para a posição especificada.

## <a name="remarks"></a>Comentários

Envie essa notificação para clientes que não escutam mensagens [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL.**](wm-vscroll.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





