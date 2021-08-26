---
title: LVN_SETDISPINFO de notificação (Commctrl.h)
description: Notifica a janela pai de um controle de exibição de lista de que ele deve atualizar as informações que mantém para um item. Esse código de notificação é enviado na forma de uma mensagem WM \_ NOTIFY.
ms.assetid: 1ea51d50-4a57-4662-972e-89e916fa9b16
keywords:
- LVN_SETDISPINFO código de notificação Windows Controles
topic_type:
- apiref
api_name:
- LVN_SETDISPINFO
- LVN_SETDISPINFOA
- LVN_SETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f4827d37a115f2bd1bb523f78bdb5975de4314056a174be4bfa886e1a076497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119915056"
---
# <a name="lvn_setdispinfo-notification-code"></a>Código de notificação LVN \_ SETDISPINFO

Notifica a janela pai de um controle de exibição de lista de que ele deve atualizar as informações que mantém para um item. Esse código de notificação é enviado na forma de uma mensagem [**WM \_ NOTIFY.**](wm-notify.md)


```C++
LVN_SETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) que especifica informações para o item alterado. O **membro** do item dessa estrutura é uma [**estrutura LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) que contém informações sobre o item que foi alterado. O **membro pszText** do **item** contém um valor válido, independentemente de o sinalizador TEXT LVIF ser definido no membro \_ **de** máscara dessa estrutura.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Sem valor de retorno.

## <a name="remarks"></a>Comentários

O receptor de notificação *lança lParam* para recuperar a [**estrutura NMLVDISPINFO.**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) O *parâmetro wParam* contém o código da mensagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVN \_ SETDISPINFOW** (Unicode) e **LVN \_ SETDISPINFOA** (ANSI)<br/>           |



## <a name="see-also"></a>Confira também

<dl> <dt>

[LVN \_ GETDISPINFO](lvn-getdispinfo.md)
</dt> </dl>

 

 





